FROM mcr.microsoft.com/dotnet/sdk:8.0.203 AS build

COPY . ./app
WORKDIR /app/
RUN dotnet build 

ENTRYPOINT ["dotnet", "run"]