FROM wisecg/rootmj:v1
LABEL maintainer "wisecg.neontetra@gmail.com"
ENV TERM xterm
WORKDIR /mjsw

# Run and remove the secret file w/ the git clone commands for MGDO & GAT (it's also ignored by git)
COPY start.sh /mjsw/
RUN ./start.sh && rm start.sh

ENV CXXFLAGS -std=c++11
ENV MGDODIR /mjsw/MGDO
ENV TAMDIR $MGDODIR/tam
ENV LD_LIBRARY_PATH $MGDODIR/lib:$LD_LIBRARY_PATH

ENV GATDIR /mjsw/GAT
ENV LD_LIBRARY_PATH=${GATDIR}/lib:${LD_LIBRARY_PATH}
ENV PATH=${GATDIR}/Apps:${GATDIR}/Scripts:${PATH}

RUN cd MGDO && ./configure --enable-majorana-all \
  && make && make install \
  && cd ../GAT && make
