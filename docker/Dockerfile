FROM fedora:30
RUN yum -y update
RUN yum -y install git make gcc g++ gtk2-devel alsa-lib-devel SDL-devel
WORKDIR /app
RUN git clone https://github.com/six519/nestopiasm.git
WORKDIR /app/nestopiasm/nesasm_3_1
RUN make
RUN cp build/nesasm ../nestopia-mod
WORKDIR /app/nestopiasm/nestopia-mod
RUN make
RUN mkdir ~/.nestopia
RUN cp nstcontrols ~/.nestopia
RUN cp NstDatabase.xml ~/.nestopia
CMD ["./nst"]
