# GO GET

manejador de paquetes de go
`go mod init hello_world_go_get_framework_echo` para inicializar go modules
`go get github.com/labstack/echo/v4` para traer el framework o libreria
`go get -v -u github.com/labstack/echo/v4` agregando -v le da verbosidad (para mostrar en pantalla todo el proceso) -u por si ya esta instalado para actualizar
`go mod tidy` para descargar dependencias que no se hayan descargado y eliminar las que no se usan
`go run .\main.go`

## CAMBIOS EN UNA LIBRERIA

- `git clone https://github.com/labstack/echo.git` para clonar la libreria a nuestro proyecto
- Hacer el cambio en los archivos descargados
- `go mod edit -replace github.com/labstack/echo/v4=./echo` para hacer el cambio en el go.mod de que ya no traiga la informacion de esa dependencia sino de los archivos que tenemos clonados en el repositorio
- `go mod edit -dropreplace github.com/labstack/echo/v4` para eliminar el reemplazo si ya no se requiere