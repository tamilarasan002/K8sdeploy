
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine3.13 as builder

WORKDIR /app

COPY CartService.csproj .

RUN dotnet restore

COPY . .

RUN dotnet publish -c Release -o /cartservice --no-restore

FROM mcr.microsoft.com/dotnet/aspnet:5.0-alpine3.13

WORKDIR /app

COPY --from=build /app/out .

EXPOSE 7070

ENV NAME Cartservice

CMD [ "dotnet", "CartService.dll" ]
