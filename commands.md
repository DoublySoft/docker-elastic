# COMANDOS DE CONFIGURACIÓN DEL ENTORNO

## AMPLIAR max_map_count DE WSL

Solución al fallo que lanza el levantamiento de los contenedores de elasticsearch en windows

```cmd
test-elasticsearch | bootstrap check failure [1] of [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
```

### ACCEDER A WSL (WINDOWS SUBSYSTEM FOR LINUX)

```cmd

wsl -d docker-desktop
```

### AMPLIAR LA CAPACIDAD DEL PARÁMETRO VIRTUAL max_map_count

```cmd
echo 262144 >> /proc/sys/vm/max_map_count
```

o

```cmd
sysctl -w vm.max_map_count=262144
```
