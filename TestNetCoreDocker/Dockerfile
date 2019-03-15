FROM microsoft/dotnet:2.1-sdk
WORKDIR /app

# copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# copy and build everything else
COPY . ./
RUN dotnet publish -c Dev -o app
#RUN dotnet publish -c Release -o /published
#RUN ls -alrth /published

#ENTRYPOINT ["dotnet", "app/TestNetCoreDocker.dll"]
ENTRYPOINT ["dotnet", "app/TestNetCoreDocker.dll"]


#/*
#Siempre compilar desplegar docker en directorio root app y con permisos de usuario admin
#*/

#docker build -t dotnetapp-dev .
#run for console.
#docker run --rm dotnetapp-dev TestNetCoreDocker from Docker
#run interactive for VSCode.
# docker run --rm -it dotnetapp-dev:latest
#docker exec -it 1ba7fd6728e7 cmd
#docker run -v $(pwd):/src -it <container_name>