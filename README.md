###### Odoo Módulo básico:



## Configuramos la database integrada en el proyecto:

![captura database](https://user-images.githubusercontent.com/92091720/226120579-35d01a43-1c23-4260-b336-498922ae18d5.png)


## Una vez hecho esto, levantamos el docker-compose:

![compose](https://user-images.githubusercontent.com/92091720/226120528-2e816469-c70a-4207-b46f-a3287e183c21.png)
## Definimos imagen del odoo, los puertos a usar tanto por éste como para postgres(por defecto), imagen de la base de datos, etc.

## Abrimos terminal en el proyecto:

```ruby 
sudo docker-compose up
```

## Odoo funcionando;

![odooFunci](https://user-images.githubusercontent.com/92091720/226120773-aab38ac2-475e-447a-aed3-7a954cc4edea.png)

### Qué pasa si el puerto 5432 para postgres está ocupado?

## Descargamos el paquete net-tools si no lo tenemos instalado ya en nuestro linux.
```ruby
sudo apt install net-tools
```

## Comprobamos si hay alguna conexión activa en el puerto 5432 con este comando
```ruby
netstat -putan | grep 5432
```
## Una vez aquí, podemos cambiar el puerto a utilizar por nuestra imagen de la base de datos, o parar el servicio que está usando nuestro puerto:
```ruby
systenctl stop postgres
