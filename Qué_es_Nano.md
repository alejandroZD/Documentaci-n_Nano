---


---

<h1 id="¿qué-es-nano">¿Qué es Nano?</h1>
<p>Nano es un protocolo de pago digital diseñado para ser accesible y ligero, enfocado en suprimir las ineficacias presentes en otras criptomonedas. Sus transacciones ultrarrápidas y sin comisiones dentro de una red segura, verde y descentralizada, hacen a Nano ideal para las transacciones diarias.</p>
<h2 id="¿cómo-funcionan-las-transacciones">¿Cómo funcionan las transacciones?</h2>
<p>Nano utiliza el Enrejado de Bloques (<a href="https://docs.nano.org/glossary/#block-lattice">Block Lattice</a>), una estructura de datos en la que las cuentas individuales controlan su propia cadena de bloques. Esto permite agregar bloques rápidamente y enviarlos a la red para su confirmación sin ningún conflicto. Las transacciones ocurren entre cuentas con dos acciones separadas:</p>
<ol>
<li>El emisor publica un bloque, el cual debita en su propia cuenta el monto que se enviará a la cuenta receptora.</li>
<li>El receptor publica un bloque correspondiente que acredita en su propia cuenta el monto enviado.</li>
</ol>
<p>Una vez que la red confirma un envío de fondos de un bloque, la transacción pasa a un estado <a href="https://docs.nano.org/glossary/#pending">pendiente</a> y no se puede revertir. El receptor puede estar desconectado y dejar los fondos en este estado de forma segura hasta que estén listos para publicar un bloque correspondiente que reciba los fondos en su cuenta.</p>
<h2 id="ligereza-bloques-con-estado">Ligereza, bloques con estado</h2>
<p>Nano utiliza una estructura para cada bloque que contiene toda la información que contiene una cuenta en ese momento: número de cuenta, saldo y representante.</p>
<p>Cada bloque también debe contener un pequeño valor de <a href="https://docs.nano.org/glossary/#proof-of-work-pow">Prueba de Trabajo</a> (POW, por sus siglas en inglés) generado por el usuario. Esto es un mecanismo de priorización de calidad de servicio que permite que las transacciones ocasionales y promedio de los usuarios se procesen de manera rápida y consistente. El cálculo de PoW para una transacción generalmente toma unos segundos en una CPU de escritorio moderna.</p>
<p>Para obtener más detalles, consulte las <a href="https://docs.nano.org/integration-guides/the-basics/">Guías de integración</a> sobre las especificaciones de los <a href="https://docs.nano.org/integration-guides/the-basics/#blocks-specifications">Bloques</a> y la <a href="https://docs.nano.org/integration-guides/the-basics/#proof-of-work">Prueba de trabajo</a>.</p>
<h2 id="representantes-y-votaciones">Representantes y votaciones</h2>
<p>Nano tiene un mecanismo de consenso único llamado <a href="https://docs.nano.org/glossary/#open-representative-voting-orv">Voto Abierto de Representante</a> (ORV, por sus siglas en inglés). Cada cuenta puede elegir libremente a un <a href="https://docs.nano.org/glossary/#representative">Representante</a> en cualquier momento para votar en su nombre, incluso cuando la cuenta delegada  está fuera de línea. Estas cuentas representantes se configuran en los nodos que permanecen en línea y votan sobre la validez de las transacciones que ven en la red. Su peso de voto es la suma de los saldos de las cuentas que les delegan, y si tienen suficiente peso de voto se convierten en <a href="https://docs.nano.org/glossary/#principal-representative">Representantes principales</a>. Los votos que envíen estos representantes principales serán posteriormente retransmitidos por otros nodos.</p>
<p>A medida que estos votos se comparten y se retransmiten entre nodos, se cuentan y se comparan con el peso de votación en línea disponible. Una vez que un nodo ve que un bloque obtiene suficientes votos para alcanzar el <a href="https://docs.nano.org/glossary/#quorum">quórum</a>, se confirma ese bloque.</p>
<p>Debido a la naturaleza ligera de los bloques y los votos, la red puede llegar a la confirmación de una transacción de manera ultrarrápida, a menudo en menos de un par de segundos. Hay que tener en cuenta que la delegación del peso de voto no significa la participación de algún fondo; la cuenta delegada aún puede gastar todos sus fondos disponibles en cualquier momento sin restricciones.</p>
<p>Debido a que las cuentas de Nano pueden delegar libremente y en cualquier momento su peso de voto a los representantes, los usuarios tienen más control sobre quién tiene poder de consenso y qué tan descentralizada está la red. Esta es una ventaja clave para el diseño del <a href="https://docs.nano.org/glossary/#open-representative-voting-orv">Voto Abierto  de Representante</a> (ORV). Sin un incentivo monetario directo para los nodos, esto elimina las fuerzas emergentes de centralización para llevarnos una tendencia a largo plazo hacia la descentralización de la red.</p>
<h2 id="ventajas-de-diseño">Ventajas de diseño</h2>
<p>Nano fue diseñado con nuevas estructuras de datos, mecanismos de consenso y otras características para obtener algunas ventajas clave sobre otras monedas digitales:</p>
<ul>
<li>El tamaño mínimo de bloque permite ligereza en la comunicación, lo que da como resultado tiempos de confirmación de transacción ultrarrápidos.</li>
<li>Sin la tradicional prueba  de trabajo y la minería, los nodos usan una energía significativamente menor a la usada por otras redes populares por cada transacción.</li>
<li>Las fuerzas de centralización emergentes para operadores de nodos se reducen debido al costo marginal cercano a cero para producir consenso en Nano|<a href="https://medium.com/@clemahieu/emergent-centralization-due-to-economies-of-scale-83cc85a7cbef">1</a></li>
</ul>
<p>Para una visión más detallada sobre el diseño de varias características del protocolo, diríjase a la <a href="https://docs.nano.org/protocol-design/overview">descripción general del diseño del protocolo</a>.</p>
<ol>
<li><a href="https://medium.com/@clemahieu/emergent-centralization-due-to-economies-of-scale-83cc85a7cbef">https://medium.com/@clemahieu/emergent-centralization-due-to-economies-of-scale-83cc85a7cbef</a></li>
</ol>

