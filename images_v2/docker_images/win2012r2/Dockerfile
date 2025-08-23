FROM ubuntu:latest

RUN apt update -y && apt install -y wget curl qemu-system-x86 qemu-utils

RUN qemu-img create -f qcow2 2012r2.img 10G

RUN wget -O- --no-check-certificate http://drive.muavps.net/windows/Windows2012r2.gz | gunzip | dd of=2012r2.img

WORKDIR /app/data

CMD ["sh", "-c", "$START"]
