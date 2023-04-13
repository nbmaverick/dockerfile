FROM ubuntu:16.04

#RUN    apt-get -y update  
#RUN    apt-get install -y unzip  
#RUN    apt-get install -y wget  

#1                install terraform
#RUN wget https://releases.hashicorp.com/terraform/1.4.5/terraform_1.4.5_linux_386.zip 
#RUN unzip terraform_1.4.5_linux_386.zip 
#RUN mv terraform /usr/local/bin/ 
#RUN terraform --version

#2                AWS CLI
#RUN DEBIAN_FRONTEND="noninteractive" apt-get update && apt-get install -y tzdata keyboard-configuration
#RUN apt-get -y install curl unzip groff less
#RUN	curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
#RUN	unzip awscliv2.zip && ./aws/install

#4                 GCLOUD
RUN apt-get update --yes \
  && apt-get install --yes curl unzip

RUN apt-get update && \
    apt-get install -y curl gnupg && \
    echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] http://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && \
    curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key --keyring /usr/share/keyrings/cloud.google.gpg  add - && \
    apt-get update -y && \
    apt-get install google-cloud-sdk -y  

#3                           Packer
# ENV PACKER_BIN_DIR /usr/local/packer/bin
# RUN mkdir --parents $PACKER_BIN_DIR 

# ENV PACKER_ZIP=https://releases.hashicorp.com/packer/0.9.0/packer_0.9.0_linux_amd64.zip
# RUN curl -sSLo /tmp/packer.zip $PACKER_ZIP && \
#  unzip /tmp/packer.zip -d $PACKER_BIN_DIR && \
#  rm /tmp/packer.zip
#ENV PATH $PATH:$PACKER_BIN_DIR
#RUN type packer

#                           Install Packer Azure
# ENV PACKER_AZURE_TAR=https://github.com/Azure/packer-azure/releases/download/prerelease/packer-azure-linux-amd64-prerelease.tar.gz

#RUN curl -sSLo /tmp/packer-azure.tar.gz $PACKER_AZURE_TAR && \
#  tar -zxvf /tmp/packer-azure.tar.gz --directory $PACKER_BIN_DIR && \
#  rm /tmp/packer-azure.tar.gz





#install packer
#install gcloud
# install AWS CLI