# Usar Usuario, Clave y Base de Datos con su propia información, por ejemplo:
# POSTGRES_USER: alvarezT        --->>> su apellido más la primera letra de su nombre
# POSTGRES_PASSWORD: tomas    --->>> una clave que ud. elija
# POSTGRES_DB: Prueba_tomas            --->>> la Base de Datos deberá tener el nombre de Prueba 

version: '1.1'

services:

  db:
    image: postgres
    restart: always
    ports:
      - "5432:5432"
    environment:
      POSTGRES_USER: alvarezT
      POSTGRES_PASSWORD: tomas
      POSTGRES_DB: Prueba_tomas

  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080
