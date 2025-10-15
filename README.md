# Project Name
### dns-paso-a-paso

# Author Name
### Francisco José Serrano Muñoz

## Configuración del archivo named.conf.options
![Configuración named.conf.options](/doc/configuración-archivo-named.conf.options.png)

## Configuración del archivo named.conf.local
![Configuración named.conf.local](/doc/configuración-archivo-named.conf.local.png)

## Creación del archivo de zona
![Creación del archivo de zona](/doc/creación-archivo-zona.png)

## Zona para la resolución inversa

### Actualización del archivo named.conf.local
![Actualización del archivo named.conf.local](/doc/update-named.conf.local.png)

### Creación de la zona inversa
![Creación del archivo de zona](/doc/creación-archivo-zona-inversa.png)

## Comprobación con dig
![Comprobación con dig](/doc/comprobación-dig.png)
#### Esta comprobación me estaba dando errores, ya que al poner la ip de windows 192.168.56.10
#### no se me conectaba al servidor.
#### He solucionado esto comprobando con la ip del servidor (127.0.0.1) y con esto he recibido
#### El resultado esperado.

## Comprobación con nslookup
![Comprobación con nslookup](/doc/comprobación-nslookup.png)

#### Aquí sucede lo mismo, el enunciado me dice que lo haga con la ip de windows,
#### pero me funciona con la ip del servidor.

<div>
    <h1>CUESTIONES FINALES</h1>
    <div>
        <h4>1. ¿Qué pasará si un cliente de una red diferente a la tuya intenta hacer uso de tu DNS de alguna manera, le funcionará? ¿Por qué, en qué parte de la configuración puede verse?</h4>
        <p>No funcionará, ya que solo permito consultas desde la red confiable.</p>
    </div>
    <div>
        <h4>2. Por qué tenemos que permitir las consultas recursivas en la configuración?</h4>
        <p>Para que el servidor pueda resolver nombres que no conoce directamente y responder con la información correcta a los clientes de la red confiable.</p>
    </div>
    <div>
        <h4>3. El servidor DNS que acabáis de montar, ¿es autoritativo?¿Por qué?</h4>
        <p>Sí, porque tiene las zonas definidas y contiene los registros maestros de (en este caso) paco.test.</p>
    </div>
    <div>
        <h4>4. ¿Dónde podemos encontrar la directiva $ORIGIN y para qué sirve?</h4>
        <p>La directiva $ORIGIN se puede encontrar en los archivos de zona. Sirve para definir el dominio base para los registros relativos.</p>
    </div>
    <div>
        <h4>5. ¿Una zona es idéntico a un dominio?</h4>
        <p>No. Una zona puede contener un dominio y sus subdominios, mientras que un dominio es solo un nombre.</p>
    </div>
    <div>
        <h4>6. ¿Cuántos servidores raíz existen?</h4>
        <p>Existen 13 servidores raíz distribuidos mundialmente.</p>
    </div>
    <div>
        <h4>7.¿Qué es una consulta iterativa de referencia?</h4>
        <p>Una consulta iterativa de referencia es una en la que el servidor devuelve referencias a otros servidores en vez de la respuesta final.</p>
    </div>
    <div>
        <h4>8. En una resolución inversa, ¿a qué nombre se mapearía la dirección IP 172.16.34.56?</h4>
        <p>Se mapearía a 56.34.16.172.in-addr.arpa</p>
    </div>
</div>