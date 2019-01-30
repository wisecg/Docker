FROM wisecg/rootmj:v2
LABEL maintainer "wisecg.neontetra@gmail.com"
ENV TERM xterm

ENV CC /usr/bin/gcc
ENV CXX /usr/bin/g++

ENV MGDODIR /global/project/projectdirs/majorana/data/mjd/surfmjd/analysis/low_e/shMGDO
ENV TAMDIR ${MGDODIR}/tam
ENV LD_LIBRARY_PATH ${MGDODIR}/install/lib:${LD_LIBRARY_PATH}

ENV GATDIR /global/project/projectdirs/majorana/data/mjd/surfmjd/analysis/low_e/shGAT
ENV LD_LIBRARY_PATH ${GATDIR}/lib:${LD_LIBRARY_PATH}
ENV PATH ${GATDIR}/Apps:${GATDIR}/Scripts:${PATH}

ENV ROOT_INCLUDE_PATH ${CLHEP_INCLUDE_DIR}:$MGDODIR/Base:$MGDODIR/Gerda:$MGDODIR/GerdaTransforms:$MGDODIR/Majorana:$MGDODIR/MJDB:$MGDODIR/Root:$MGDODIR/Tabree:$MGDODIR/Tools:$MGDODIR/Transforms:$TAMDIR:$TAMDIR/inc:$GATDIR/BaseClasses:$GATDIR/MGTEventProcessing:$GATDIR/MGOutputMCRunProcessing:$GATDIR/SiggenWrapper