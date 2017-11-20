# docker-calibre-server

Generic calibre-server docker container. By default, this calibre-server enables
authentication and expects the library at "/calibre" and the user authentication
database at "/calibre/user.db". There, the container expects a volume with the
library and user database to be mounted at that location.

If the library is on the location machine at "/my-local-library" then you can
create and manage a user database interactively using:
```bash
docker run -ti --rm -v "/my-local-library:/calibre" cjhardekopf/calibre-server --userdb /calibre/user.db --manage-users
```
You can run calibre-server with the default options using:
```bash
docker run -ti --rm -v "/my-local-library:/calibre" cjhardekopf/calibre-server
```

