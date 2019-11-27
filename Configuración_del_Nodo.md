---


---

<h1 id="configuración-del-nodo">Configuración del nodo</h1>
<p>Si bien puede correr un nodo de Nano descargando un binario o desarrollandolo desde la fuente, se recomienda usar un contenedor Docker. Al usar las <a href="https://hub.docker.com/r/nanocurrency/nano/tags/">imágenes oficiales de Docker</a>, su nodo será mucho más fácil de actualizar y mantener.</p>
<h2 id="warning-limitaciones-de-docker">⚠️ Limitaciones de Docker</h2>
<p>Aunque Docker es una buena opción para muchas configuraciones, hay algunas limitaciones a tener en cuenta:</p>
<ul>
<li>No se recomienda correr un contenedor *nix, como el proporcionado oficialmente, en un host de Windows; se conocen problemas con el manejo de puertos que impiden la comunicación adecuada con sus pares.</li>
<li>V19 y más bajas: Debido a la secuencia de comandos de inicio integrada en los contenedores Docker, las <a href="https://docs.nano.org/commands/command-line-interface/#launch-options">opciones de inicio</a> para el servicio <code>nano_node</code> que se ejecutan dentro del contenedor no se pueden usar fácilmente. Estas opciones están disponibles a partir de la V20.</li>
</ul>
<h2 id="pencil2-supuestos-de-configuración">✏️ Supuestos de configuración</h2>
<p>Las guías que se encuentran en este sitio hacen algunas suposiciones básicas que deben entenderse antes de continuar:</p>
<ul>
<li>Tiene una comprensión básica de Docker.</li>
<li>Está utilizando las <a href="https://hub.docker.com/r/nanocurrency/nano/tags/">imágenes oficiales del Docker de Nano</a> para administrar su nodo. Si decide utilizar un método diferente, deberá ser capaz de completar los espacios en blanco durante el proceso.</li>
</ul>
<h2 id="fire-configuración-de-la-red-beta">🔥 Configuración de la red beta</h2>
<p>Los detalles a continuación se centran en correr un nodo en la red principal. La red beta también está disponible para pruebas y es un excelente lugar para aprender sobre el manejo de los nodos. Los nodos beta también ayudan a mejorar nuestra red, así que considere correr uno.</p>
<p>Consulte la página de la <a href="https://docs.nano.org/running-a-node/beta-network/">Red Beta</a> para obtener detalles sobre cómo configurar un nodo en esta red de prueba.</p>
<h2 id="hardware-recomendado">Hardware recomendado</h2>
<h2 id="nodo-de-representante-principal">Nodo de Representante Principal</h2>
<p>Las siguientes son especificaciones mínimas recomendadas para nodos con más del 0.1% del peso de votación en línea (<a href="https://docs.nano.org/glossary/#principal-representative">Representantes principales</a>):</p>
<ul>
<li>
<p>4GB de RAM</p>
</li>
<li>
<p>CPU de cuatro núcleos</p>
</li>
<li>
<p>Ancho de banda de 250 MB/s (2TB de ancho de banda disponibles al mes)</p>
</li>
<li>
<p>Disco duro basado en SSD</p>
</li>
</ul>
<h2 id="nodo-de-representante">Nodo de Representante</h2>
<p>Las siguientes son especificaciones mínimas recomendadas para nodos con menos del 0.1% del peso de votación en línea (<a href="https://docs.nano.org/glossary/#representative">Representantes</a> regulares):</p>
<ul>
<li>
<p>2GB de RAM</p>
</li>
<li>
<p>CPU de doble núcleo</p>
</li>
<li>
<p>Ancho de banda de 100 MB/s (1TB de ancho de banda disponible al mes)</p>
</li>
<li>
<p>Disco duro basado en SSD</p>
</li>
</ul>
<h2 id="⚠️-advertencia">⚠️ Advertencia</h2>
<p>Varios factores afectan el uso de recursos, incluida la frecuencia con la que se realizan llamadas RPC, otras aplicaciones que se ejecutan en la máquina, etc. Estas recomendaciones deben evaluarse junto con otras consideraciones.</p>
<h2 id="🔥-generación-de-prueba-de-trabajo">🔥 Generación de Prueba de Trabajo</h2>
<p>Para los nodos que se utilizan con servicios que requieren el envío y la recepción de transacciones de un volumen alto o regular, se deben hacer consideraciones especiales para manejar las actividades de generación de Prueba de trabajo.</p>
<p>Las GPU proporcionan un rendimiento mucho mayor que las CPU. Los <a href="https://docs.nano.org/running-a-node/configuration/#work_peers">pares de trabajo</a> también se pueden configurar para generar trabajo fuera del nodo.</p>
<h2 id="puertos-de-red">Puertos de red</h2>
<p>El <code>nano_node</code> utilizará dos puertos configurables a lo largo de su ciclo de vida. Los valores predeterminados sugeridos por los <a href="https://docs.nano.org/running-a-node/configuration/#network-details">detalles de la red</a> son los siguientes:</p>
<h2 id="ℹ️-descripción-general-de-los-puertos-de-red">ℹ️ Descripción general de los puertos de red</h2>
<ul>
<li>
<p>7075 UDP : para actividad de la <a href="https://docs.nano.org/glossary/#live-network">red en vivo</a> (respaldo desde la V19.0)</p>
</li>
<li>
<p>7075 TPC: para actividad de la <a href="https://docs.nano.org/glossary/#live-network">red en vivo</a> (desde la V19.0) y actividad de la <a href="https://docs.nano.org/glossary/#bootstrap-network">red de arranque</a>.</p>
</li>
<li>
<p>7076 TCP: para comunicación con el servidor RPC. <strong>No exponga esto fuera de su entorno de producción. Cualquier persona con acceso a este puerto puede controlar el RPC de su nodo.</strong></p>
</li>
</ul>
<p>El nano_node intentará usar UPnP por defecto. <a href="https://docs.nano.org/running-a-node/troubleshooting/#troubleshooting-upnp">La información sobre resolución de problemas se puede encontrar aquí</a>.</p>
<h2 id="instalación-del-docker">Instalación del Docker</h2>
<p>El Docker debe estar instalado en la máquina anfitriona y las instrucciones se pueden encontrar aquí: <a href="https://docs.docker.com/install/">https://docs.docker.com/install/</a>. Recomendamos instalar la última versión estable disponible.</p>
<h2 id="descarga-de-imagen-docker">Descarga de imagen Docker</h2>
<p><img src="https://img.shields.io/docker/pulls/nanocurrency/nano.svg" alt="Docker Pulls"><br>
La imagen Docker se puede descargar a través de <code>Docker Pull</code>. Podemos tomar la versión/etiqueta <code>más reciente</code> o específica. No se especifica una etiqueta por defecto a la <code>más reciente</code>. Un ejemplo de cada una se encuentra a continuación.</p>
<p>Descarga la versión más reciente del nodo de Nano:</p>
<pre><code>docker pull nanocurrency/nano
</code></pre>
<p>Descarga una versión específica del nodo de Nano:</p>
<pre><code>docker pull nanocurrency/nano:V18.0
</code></pre>
<h2 id="fire-tip">🔥 Tip</h2>
<p>Si está corriendo un nodo en un entorno empresarial, se recomienda que especifique explícitamente la versión estable más reciente para garantizar contenedores deterministas. Se puede encontrar una lista de etiquetas en el <a href="https://hub.docker.com/r/nanocurrency/nano/tags/">Nano Currency Docker Hub</a> oficial.</p>
<h2 id="warning-configuración-de-multiples-nodos">⚠️ Configuración de multiples nodos</h2>
<p><strong>Nunca</strong> use la misma semilla en varias instancias del nano_node corriendo al mismo tiempo.</p>
<ul>
<li>Múltiples nano_nodos que usan la misma semilla pueden generar condiciones de carrera en la red que degradan el rendimiento de sus cuentas personales.</li>
<li>Además, la publicación de transacciones de dos nodos con la misma cuenta al mismo tiempo puede causar una bifurcación de cuenta que requiere un proceso más lento de votación del representante.</li>
<li>Del mismo modo, si está corriendo una cuenta representante en varios nodos, pueden publicar votos conflictivos, lo que hace que su representante sea ignorado por la red.</li>
<li>La degradación del rendimiento en entornos empresariales puede ser significativa.</li>
</ul>
<h2 id="inicio-del-nodo">Inicio del nodo</h2>
<p>Con Docker hay comandos básicos para administrar contenedores. Para activar correctamente el nodo, aprenda estos comandos comenzando con el <a href="https://docs.nano.org/running-a-node/docker-management#starting">inicio del contenedor</a>.</p>
<h2 id="information_source-programación-avanzada">ℹ️ Programación avanzada</h2>
<p>Para obtener opciones adicionales sobre cómo programar el nodo para que corra en varias plataformas, diríjase a las <a href="https://docs.nano.org/integration-guides/build-options">Guías de integración para opciones de programación</a>.</p>

