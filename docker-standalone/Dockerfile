FROM debian
RUN apt update && apt install wget aria2 git bzip2 -y
RUN git clone --recursive https://github.com/henk717/koboldai /opt/koboldai
WORKDIR /opt/koboldai
RUN ./install_requirements.sh cuda
COPY docker-helper.sh /opt/koboldai/docker-helper.sh
RUN chmod +x /opt/koboldai/docker-helper.sh
EXPOSE 5000/tcp
ENV githubaddress=https://github.com/henk717/KoboldAI
ENV githubbranch=united
ENV install_packages=true
CMD /opt/koboldai/docker-helper.sh
