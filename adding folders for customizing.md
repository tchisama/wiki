





# docker-compose-file without any extra needed

```yaml
version: '3.1'
services:
  web:
    image: odoo:15
    depends_on:
      - db // all the services that are needed to be up before this service
      
    ports:
      - "8069:8069"
    environment:
      - HOST=db
      - USER=odoo
      - PASSWORD=odoo
  db:
    image: postgres:15
    ports:
      - "5432:5432"
    environment:
      POSTGRES_DB: postgres
      POSTGRES_USER: odoo
      POSTGRES_PASSWORD: odoo
```


# make env files for the services (odoo , postgress)


```env
# odoo.env
HOST=db
USER=odoo
PASSWORD=odoo
```

```env
# db.env
POSTGRES_DB=postgres
POSTGRES_USER=odoo
POSTGRES_PASSWORD=odoo
```

# QA 

1 how to change the name of docker compose project name?
```env
COMPOSE_PROJECT_NAME=odoo
```
2 how to use env variables inside the docker-compose-file?
```yaml
version: '3.1'
services:
  web:
    image: odoo:15
    depends_on:
      - db // all the services that are needed to be up before this service
      
    ports:
      - "8069:8069"
    environment:
      - HOST=${HOST}
      - USER=${USER}
      - PASSWORD=${PASSWORD}
  db:
    image: postgres:15
    ports:
      - "5432:5432"
    // or u can use a .env file diractly
    env_file:
      - [db env](./db.env)
```




# odoo docker network

```yaml
version: '3.1'
services:
  web:
    image: odoo:15
    depends_on:
    networks:
      - odoo_network
    ports:
      - "8069:8069"
    environment:
      - HOST=db
      - USER=odoo
      - PASSWORD=odoo
  db:
    image: postgres:15
    networks:
      - odoo_network
    ports:
      - "5432:5432"
    environment:
      POSTGRES_DB: postgres
      POSTGRES_USER: odoo
      POSTGRES_PASSWORD: odoo
networks:
  odoo_network:
    driver: bridge
```


# odoo docker volumes

```yaml
version: '3.1'






services:
  web:
    image: odoo:15
    depends_on:
    networks:
      - odoo_network
    ports:
      - "8069:8069"
    environment:
      - HOST=db
      - USER=odoo
      - PASSWORD=odoo
    volumes:
      - odoo-web-data:/var/lib/odoo
  db:
    image: postgres:15
    networks:
      - odoo_network
    ports:
      - "5432:5432"
    environment:
      POSTGRES_DB: postgres
      POSTGRES_USER: odoo
      POSTGRES_PASSWORD: odoo
    volumes:
      - odoo-db-data:/var/lib/postgresql/data
networks:
  odoo_network:
    driver: bridge
volumes:
  odoo-web-data:
  odoo-db-data:
```































