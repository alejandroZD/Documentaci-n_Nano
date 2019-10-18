---


---

<h1 id="introducción">Introducción</h1>
<p>Correr un nodo es una manera clave de ayudar a descentralizar la red y proporcionar un punto de acceso a la red para sistemas construidos sobre Nano. Antes de configurar un nodo, recomendamos revisar los siguientes detalles para tener una mejor comprensión sobre las motivaciones para su puesta en marcha, el mantenimiento requerido, los tipos y las especificaciones recomendadas.</p>
<h1 id="¿por-qué-correr-un-nodo">¿Por qué correr un nodo?</h1>
<p>Por diseño, los incentivos por correr un nodo de Nano no se encuentran dentro de la red, sino que son externos. Esta es una diferencia importante en comparación con casi todas las demás redes de criptomonedas y permite a Nano operar de forma segura y sin comisiones por transacción. <a href="https://medium.com/nanocurrency/the-incentives-to-run-a-node-ccc3510c2562">1</a>|<a href="https://medium.com/@clemahieu/emergent-centralization-due-to-economies-of-scale-83cc85a7cbef">2</a> Estos incentivos externos e indirectos incluyen lo siguiente y más:</p>
<ul>
<li>Exposición publicitaria de su representante, mostrándolo en selectas listas de representantes.</li>
<li>Ahorro en comisiones para empresas y organizaciones que aceptan Nano como método de pago.</li>
<li>Tener un punto de acceso confiable para desarrollar software adicional en la red.</li>
</ul>
<p>Independientemente de la motivación que se tenga para correr un nodo, solo beneficiará a la red si se tiene el cuidado adecuado para garantizar que se corra en máquinas correctamente aprovisionadas y se le haga mantenimiento continuo al nodo, al sistema operativo y a cualquiera de los sistemas de soporte de manera rutinaria.</p>
<h1 id="tipos-de-nodos">Tipos de nodos</h1>
<h2 id="nodos-de-representantes-principales">Nodos de Representantes Principales</h2>
<p>Actualmente, los nodos configurados con cuentas de Representantes con al menos el 0.1% del <a href="https://docs.nano.org/glossary/#online-voting-weight">peso de votación en línea</a> delegado a ellos, participan más ampliamente en el consenso de la red porque envían votos a sus pares, quienes los retransmiten posteriormente.</p>
<h2 id="convertirse-en-representante-principal">Convertirse en Representante principal</h2>
<p>Incluso una cuenta que hoy no tiene peso, con el tiempo puede convertirse en un Representante principal, gracias a la capacidad que tiene cualquier usuario dentro de la red de redelegar su peso de voto.</p>
<h2 id="nodos-de-representantes">Nodos de Representantes</h2>
<p>Los nodos con menos del 0.1% del <a href="https://docs.nano.org/glossary/#online-voting-weight">peso de votación en línea</a> validarán y votarán las transacciones vistas en la red; sin embargo, sus votos no serán retransmitidos por otros pares.</p>
<h1 id="recursos-y-mantenimiento-continuo">Recursos y mantenimiento continuo</h1>
<p>Los nodos consumen recursos de CPU, RAM, entrada y salida del disco duro y ancho de banda, todo lo cual tiene un costo. Para mantener el nodo sincronizado y participando, se deben seguir las especificaciones recomendadas a continuación para máquinas basadas en el tipo de nodo.</p>
<h2 id="recomendaciones-de-hardware">Recomendaciones de hardware</h2>
<h2 id="nodo-de-representante-principal">Nodo de Representante principal</h2>
<p>Las siguientes son especificaciones mínimas recomendadas para nodos con más del 0.1 % del peso de votación en línea (<a href="https://docs.nano.org/glossary/#principal-representative">Representantes principales</a>):</p>
<ul>
<li>4GB de RAM</li>
<li>CPU de cuatro núcleos</li>
<li>Ancho de banda de 250 MB/s (2TB de ancho de banda mensual disponible)</li>
<li>Disco duro basado en SSD</li>
</ul>
<h2 id="nodo-de-representante">Nodo de Representante</h2>
<p>Las siguientes son especificaciones mínimas recomendadas para nodos con menos del 0.1 % del peso de votación en línea (<a href="https://docs.nano.org/glossary/#representative">Representantes</a> regulares):</p>
<ul>
<li>2GB de RAM</li>
<li>CPU de doble núcleo</li>
<li>Ancho de banda de 100 MB/s (1TB de ancho de banda mensual disponible)</li>
</ul>
<h2 id="warning-advertencia">⚠️ Advertencia</h2>
<p>Varios factores afectan el uso de recursos, incluida la frecuencia con la que se realizan llamadas RPC, otras aplicaciones que se ejecutan en la máquina, etc. Estas recomendaciones deben evaluarse junto con otras consideraciones.</p>
<h2 id="fire-generación-de-prueba-de-trabajo">🔥 Generación de Prueba de Trabajo</h2>
<p>Para los nodos que se utilizan con servicios que requieren un volumen alto o regular de envío y recepción de transacciones, se deben hacer consideraciones especiales para manejar las actividades de generación de Prueba de Trabajo.<br>
Las GPU proporcionan un rendimiento mucho mayor que las CPU. Los <a href="https://docs.nano.org/running-a-node/configuration/#work_peers">pares de trabajo</a> también se pueden configurar para generar trabajo fuera del nodo.<br>
Y con cualquier sistema, se debe tener en cuenta el mantenimiento continuo para evitar problemas:</p>
<ul>
<li>Realizar actualizaciones a nivel de sistema operativo y aplicar regularmente parches de seguridad.</li>
<li>Actualizar el nodo a las últimas versiones que estén disponibles.</li>
<li>Seguir los mejores métodos para proteger contraseñas u otros datos confidenciales relacionados con el nodo.</li>
</ul>
<p>Si no se tiene cuidado con la seguridad y el mantenimiento de los sistemas que alojan al nodo, se podría perder cualquier beneficio a la red.</p>
<ol>
<li><a href="https://medium.com/nanocurrency/the-incentives-to-run-a-node-ccc3510c2562">https://medium.com/nanocurrency/the-incentives-to-run-a-node-ccc3510c2562</a></li>
<li><a href="https://medium.com/@clemahieu/emergent-centralization-due-to-economies-of-scale-83cc85a7cbef">https://medium.com/@clemahieu/emergent-centralization-due-to-economies-of-scale-83cc85a7cbef</a></li>
</ol>

