FROM centos:7

RUN yum -y install libunwind libicu && curl -sSL -o dotnet.tar.gz https://go.microsoft.com/fwlink/?LinkID=827529 && mkdir -p /opt/dotnet && tar zxf dotnet.tar.gz -C /opt/dotnet && ln -s /opt/dotnet/dotnet /usr/local/bin && yum clean all


