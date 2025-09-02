# Configuracion

## Dependencias

```sh
python=3.11.8
```

- No es necesario instalar localstack, ya que se trabajara mediando `docker-compose.yml`

## Levantar contenedor

```sh
docker-compose up
```

## Instalaciones necesarias

[AWS CLI 2](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

- En donde segun tus necesidades se descarga para windows, macOS o linux

[**Documentacion AWS CLI 2**](https://docs.aws.amazon.com/cli/latest/)

### Congiguracion de AWS CLI

Para configurar un asuario, y no tener este error:

```sh
$ aws --endpoint-url http://localhost:4566 s3 ls

Unable to locate credentials. You can configure credentials by running "aws configure".
```

Configuracion de perfil

```sh
$ aws configure --profile [nombe-perfil]
```

- El nombre del perfil puede ser ficticio
  **Esto se hace para hacer crear un perfil**

### EROR: Unable to locate credentials.

Si se sigue recibiendo el mensaje:

```sh
$ aws --endpoint-url http://localhost:4566 s3 ls

Unable to locate credentials. You can configure credentials by running "aws configure".
```

ejecutar `aws configure` y llenar lo que se pide(ficticio)

```sh
$ aws configure
AWS Access Key ID [None]: test
AWS Secret Access Key [None]: test
Default region name [None]: us-east-1
Default output format [None]: json
```
