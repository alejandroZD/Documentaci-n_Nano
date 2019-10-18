---


---

<h1 id="glosario">Glosario</h1>
<h2 id="altura-del-bloque-block-height">Altura del bloque (<a href="https://docs.nano.org/glossary/#block-height">Block height</a>)</h2>
<p>Un valor local entero que representa el orden de un bloque en una cadena de cuentas. Por ejemplo, el bloque 15 en una cuenta tendría una altura de bloque de 15. Relacionado con (pero diferente de) la altura de confirmación.</p>
<h2 id="altura-de-confirmación-confirmation-height">Altura de confirmación (<a href="https://docs.nano.org/glossary/#confirmation-height">Confirmation height</a>)</h2>
<p>Un número almacenado en la base de datos local del nodo que representa el bloque confirmado más alto (más reciente) en una cadena de cuentas. Relacionado con (pero diferente de) la altura del bloque.</p>
<h2 id="billetera-wallet">Billetera (<a href="https://docs.nano.org/glossary/#wallet">wallet</a>)</h2>
<p>Una billetera es un objeto organizacional en un nano_node que contiene una sola semilla de la cual se derivan de manera determinística varias cuentas a través de un índice uint32 que comienza en 0. Las llaves privadas se derivan de la semilla y el índice de la siguiente manera:</p>
<pre><code>Llave privada = blake2b (semilla||índice)
</code></pre>
<h2 id="bloque-block">Bloque (Block)</h2>
<p>Una sola transacción de Nano. Todas las nuevas transacciones (por ejemplo, envíos, recibos, cambios de representante, etc.) en el protocolo Nano se comunican a través de bloques con estado (desde el nodo V11). El estado completo de la cuenta, incluido el saldo después de cada transacción, se registra en cada bloque. Los montos de las transacciones se interpretan como la diferencia de saldo entre bloques consecutivos. Antes de la V11, cada tipo de transacción (abrir, enviar, recibir, cambiar) tenía su propio tipo de bloque heredado.</p>
<h2 id="bloque-cabecero-head-block"><s>Bloque cabecero</s> (<a href="https://docs.nano.org/glossary/#head-block">head block</a>)</h2>
<p>Ver puntero.</p>
<h2 id="bloques-heredados-legacy-blocks">Bloques heredados (<a href="https://docs.nano.org/glossary/#legacy-blocks">legacy blocks</a>)</h2>
<p>Bloques en una cadena de cuentas antes del primer bloque v1 (suele ser el bloque de la época v1 pero puede ser de otros tipos). El primer bloque v1 y todos los bloques posteriores son bloques con estado.</p>
<h2 id="bloques-por-segundo-bps-blocks-per-second">Bloques por segundo (BPS) (<a href="https://docs.nano.org/glossary/#blocks-per-second-bps">Blocks Per Second</a>)</h2>
<p>La tasa de transmisión de bloques no confirmados (transacciones) en la red.</p>
<h2 id="cementación-cementing">Cementación (<a href="https://docs.nano.org/glossary/#cementing">cementing</a>)</h2>
<p>Cuando un nodo específico marca una transacción confirmada como localmente irreversible al configurar la altura de confirmación de la cuenta (en la base de datos de nodos) con la nueva altura de bloque más alta de la transacción confirmada. La cementación es una operación a nivel de nodo.</p>
<h2 id="confirmación-confirmation">Confirmación (<a href="https://docs.nano.org/glossary/#confirmation">confirmation</a>)</h2>
<p>Cuando un bloque (transacción) reúne suficientes votos en la red para aprobar el quórum. Tenga en cuenta que los envíos confirmados son irreversibles (es decir, totalmente liquidados), pero el receptor debe publicar un bloque de recepción correspondiente antes de poder gastar los fondos pendientes. La confirmación es una decisión a nivel de red.</p>
<h2 id="confirmaciones-por-segundo-cps-confirmation-per-second">Confirmaciones por segundo (CPS) (<a href="https://docs.nano.org/glossary/#confirmations-per-second-cps">Confirmation per second</a>)</h2>
<p>La tasa de bloques confirmados (enviados o recibidos).</p>
<h2 id="cuenta-account">Cuenta (<a href="https://docs.nano.org/glossary/#account">account</a>)</h2>
<p>Se refiere a una dirección (comienza con xrb_ o nano_, los prefijos son intercambiables) de la cual usted controla las llaves privadas. Una dirección es una reinterpretación de la llave pública de 256 bits mediante la codificación BASE32 y una suma de comprobación. El prefijo xrb- soportado anteriormente, se encuentra en desuso.</p>
<h2 id="cuentas-ad-hoc-ad-hoc-accounts">Cuentas ad hoc (<a href="https://docs.nano.org/glossary/#ad-hoc-accounts">ad hoc accounts</a>)</h2>
<p>Cuentas no derivadas de una semilla privada que se puede mantener en la billetera del nodo a través de la identificación de la billetera. Se recomienda el uso de estas cuentas solo con sistemas avanzados.</p>
<h2 id="cuenta-sin-abrir-unopened-account">Cuenta sin abrir (<a href="https://docs.nano.org/glossary/#unopened-account">unopened account</a>)</h2>
<p>Una dirección de cuenta que no tiene un primer bloque (debe ser un bloque para recibir Nano enviados desde otra cuenta, no puede ser un bloque que solo cambie al Representante).</p>
<h2 id="diferido-unpocketed">Diferido (<a href="https://docs.nano.org/glossary/#unpocketed">unpocketed</a>)</h2>
<p>Ver pendiente.</p>
<h2 id="elección-election">Elección (<a href="https://docs.nano.org/glossary/#election">election</a>)</h2>
<h2 id="enrejado-de-bloques-block-lattice">Enrejado de bloques (<a href="https://docs.nano.org/glossary/#block-lattice">Block Lattice</a>)</h2>
<p>El enrejado de bloques es una estructura de datos en la que las cuentas individuales controlan su propia cadena de bloques. Esto permite agregar transacciones rápidamente, sin conflictos y enviarlas a la red para su confirmación.</p>
<h2 id="envío-entrante-inbound-send">Envío entrante (<a href="https://docs.nano.org/glossary/#inbound-send">inbound send</a>)</h2>
<p>Un bloque con fondos que se transfiere a una cuenta que pertenece a una billetera de su nodo.</p>
<h2 id="frontier-frontier"><s>Frontier</s> (<a href="https://docs.nano.org/glossary/#frontier">Frontier</a>)</h2>
<p>El bloque más reciente agregado a la cadena de cuentas. También se le llama bloque cabeza. Puede ser confirmado o no confirmado.</p>
<h2 id="génesis-genesis">Génesis (<a href="https://docs.nano.org/glossary/#genesis">genesis</a>)</h2>
<h2 id="hash-del-bloque-block-hash">Hash del bloque (<a href="https://docs.nano.org/glossary/#block-hash">Block hash</a>)</h2>
<p>Un valor de cadena hexadecimal de 64 caracteres en mayúsculas (0-9 A-F) que representa un bloque único en una cuenta.</p>
<h2 id="identificación-de-la-billetera-wallet-id">Identificación de la billetera (<a href="https://docs.nano.org/glossary/#wallet_id">Wallet ID</a>)</h2>
<p>Un nombre / identificador de un valor aleatorio de 256 bits para una billetera específica en la base de datos local nano_node. La identificación de la billetera no se almacena en ningún lugar de la red y solo se usa en el nano_node local. Aunque una identificación de billetera parece idéntica a una semilla, no se deben confundir; los fondos no se pueden restaurar con una identificación de billetera. No respalde la identificación de la billetera como un medio para respaldar fondos.</p>
<h2 id="pares-peers">Pares (<a href="https://docs.nano.org/glossary/#peers">peers</a>)</h2>
<p>Nodos conectados a través del Internet público para compartir datos de la red Nano.</p>
<h2 id="pares-de-trabajo-work-peers">Pares de trabajo (<a href="https://docs.nano.org/glossary/#work-peers">work peers</a>)</h2>
<p>Pares de nodos que están configurados para generar trabajo para las transacciones a petición originaria de los nodos.</p>
<h2 id="pendiente-pending">Pendiente (<a href="https://docs.nano.org/glossary/#pending">pending</a>)</h2>
<p>Un estado de transacción en el que la red publicó y confirmó un bloque que envía fondos, pero aún no se ha confirmado un bloque coincidente que reciba esos fondos.</p>
<h2 id="peso-de-votación-voting-weight">Peso de votación (<a href="https://docs.nano.org/glossary/#voting-weight">voting weight</a>)</h2>
<p>La cantidad de peso delegada a un Representante.</p>
<h2 id="peso-de-votación-en-línea-online-voting-weight">Peso de votación en línea (<a href="https://docs.nano.org/glossary/#online-voting-weight">Online voting weight</a>)</h2>
<p>También llamado participación en línea, es un valor de tendencia. El nodo muestrea ponderaciones de los representantes en línea cada 5 minutos por un período continuo de 2 semanas. El valor del peso de la votación en línea es el promedio de esas muestras.</p>
<h2 id="prueba-de-trabajo-proof-of-work---pow">Prueba de trabajo (<a href="https://docs.nano.org/glossary/#proof-of-work-pow">Proof of Work - PoW</a>)</h2>
<p>Una prueba de trabajo es una pieza de datos que satisface ciertos requisitos y es difícil (costoso, lento) de producir, pero fácil de verificar para otros. En algunos sistemas, estos datos son una parte central del modelo de seguridad utilizado para proteger contra el doble gasto y<br>
otros tipos de ataques, pero con Nano solo se usa para aumentar los costos económicos de enviar spam a la red.</p>
<h2 id="quórum-quorum">Quórum (<a href="https://docs.nano.org/glossary/#quorum">quorum</a>)</h2>
<p>Cuando el delta entre los dos bloques sucesivos de una raíz es &gt; 50% del peso de la votación en línea.</p>
<h2 id="raíz-root">Raíz (<a href="https://docs.nano.org/glossary/#root">Root</a>)</h2>
<p>La cuenta si el bloque es el primer bloque de la cuenta; de lo contrario, es el hash anterior incluido en el bloque.</p>
<h2 id="red-de-arranque-bootstrap-network">Red de arranque (<a href="https://docs.nano.org/glossary/#bootstrap-network">Bootstrap network</a>)</h2>
<p>Una subred establecida entre pares a través del Protocolo de Control de Transmisión (TCP, por sus siglas en inglés) para gestionar la transmisión masiva de bloques. Esta se usa en la sincronización de arranque inicial de los pares y cuando los pares no sincronizados intentan llenar grandes espacios en sus libros mayores distribuidos. Está disponible en todas las redes Nano (redes principales, beta y de prueba).</p>
<h2 id="red-en-vivo-live-network">Red en vivo (<a href="https://docs.nano.org/glossary/#live-network">live network</a>)</h2>
<p>Una subred establecida entre pares a través del Protocolo de datagramas de usuario (UDP, por sus siglas en inglés) para comunicar bloques publicados recientemente, votos y otro tráfico no relacionado con la sincronización de arranque. Está disponible en todas las redes Nano (redes principales, beta y de prueba).</p>
<h2 id="representante-representative">Representante (<a href="https://docs.nano.org/glossary/#representative">Representative</a>)</h2>
<p>Una cuenta de Nano con &gt; 0 peso de votación, pero &lt;0.1% del peso de votación en línea delegada a ella. A diferencia de los Representantes principales, cuando se configura en un nodo que vota, los votos que produce y envía a sus pares directamente conectados, no serán retransmitidos por esos pares.</p>
<h2 id="representante-principal-principal-representative">Representante principal (<a href="https://docs.nano.org/glossary/#principal-representative">Principal Representative</a>)</h2>
<p>Una cuenta de Nano con &gt; = 0.1% del peso de votación en línea delegado a ella. Cuando se configura en un nodo que está votando, los votos que produce serán retransmitidos por otros nodos a quienes los reciban, ayudando a la red a llegar a un consenso más rápidamente.</p>
<h2 id="rondas-de-anuncios-announcement-rounds">Rondas de anuncios (<a href="https://docs.nano.org/glossary/#announcement-rounds">announcement rounds</a>)</h2>
<p>Un ciclo repetitivo de 16 segundos en el nodo durante el cual se recogen los votos para las transacciones activas en un intento por alcanzar el quórum.</p>
<h2 id="semilla-seed">Semilla (<a href="https://docs.nano.org/glossary/#seed">seed</a>)</h2>
<p>Un valor aleatorio de 256 bits generalmente representado para el usuario como un valor hexadecimal de 64 caracteres (0-9 y A-F). Las llaves privadas se derivan de una semilla.</p>
<h2 id="sincronización-de-arranque-bootstrapping">Sincronización de Arranque (<a href="https://docs.nano.org/glossary/#bootstrapping">bootstrapping</a>)</h2>
<p>Durante la sincronización inicial, el nano_node solicita transacciones antiguas para verificar y completar de forma independiente su base de datos del libro mayor distribuido local. La sincronización de arranque también tendrá lugar cuando el nano_node no esté sincronizado con la red.</p>
<h2 id="sin-revisión-bloques-unchecked-blocks">Sin revisión (bloques) (<a href="https://docs.nano.org/glossary/#unchecked-blocks">unchecked blocks</a>)</h2>
<h2 id="suministro-circulante-circulating-supply">Suministro circulante (<a href="https://docs.nano.org/glossary/#circulating-supply">circulating supply</a>)</h2>
<p>133,248,297.920938463463374607431768211455 Nano. Este es el suministro que resultó después de que se hiciera una quema desde la cuenta génesis, la cuenta receptora y la cuenta del grifo, de acuerdo con la distribución original. El suministro circulante real es menor debido a la pérdida de llaves y envíos a cuentas quemadas. El suministro original menos las cantidades enviadas a la cuenta de quema se puede encontrar utilizando el RPC de suministro disponible.</p>
<h2 id="transacción-activa-active-transaction">Transacción activa (<a href="https://docs.nano.org/glossary/#active-transaction">Active transaction</a>)</h2>
<p>Bloque recién descargado al nodo que entra en el proceso de votación.</p>
<h2 id="transacciones-por-segundo-tps-transactions-per-second">Transacciones por segundo (TPS) (<a href="https://docs.nano.org/glossary/#transactions-per-second-tps">transactions per second</a>)</h2>
<p>A menudo se usa para referirse a la tasa de transacciones completadas entre dos partes (es decir, un envío con la recepción correspondiente). En el pasado, TPS era una medición por nodo que representaba la tasa de transmisión percibida a nivel de red (BPS), pero se descubrió que esta medición era algo imprecisa debido a las diferencias de interconexión y propagación entre nodos.TPS ahora se usa para referirse a (Confirmaciones por segundo/2) que es más similar a la métrica TPS utilizada por otras criptomonedas (por ejemplo, Bitcoin). Los envíos de<br>
Nano no requieren que se confirme la recepción correspondiente, pero los bloques de recepción deben confirmarse antes de que los fondos recibidos puedan enviarse nuevamente (ver pendiente).</p>
<h2 id="voto-abierto-de-representante-orv-open-representative-vote">Voto Abierto de Representante (ORV) (<a href="https://docs.nano.org/glossary/#open-representative-voting-orv">Open Representative Vote</a>)</h2>
<p>Un mecanismo de consenso exclusivo de Nano que implica que las cuentas deleguen su saldo como peso de voto a los Representantes. Los Representantes votan sobre la validez de las transacciones publicadas en la red utilizando el peso de voto que se les delega. Estos votos se comparten con sus pares directamente conectados y también retransmiten los votos vistos por los Representantes Principales. Los votos se cuentan y una vez que se alcanza el quórum en un bloque publicado, la red lo considera confirmado.</p>
<h2 id="votación-voting">Votación (<a href="https://docs.nano.org/glossary/#voting">Voting</a>)</h2>
<p>Cada nodo configurado con un Representante vota en cada bloque agregando su firma de Representante y un número de secuencia al hash. Estos se enviarán a pares directamente conectados y, si el voto se origina de un Representante Principal, posteriormente será reenviado por los nodos a sus pares.</p>
<h2 id="voto-por-hash-vote-by-hash">Voto por hash (<a href="https://docs.nano.org/glossary/#vote-by-hash">Vote-by-hash</a>)</h2>
<p>Permite a los representantes incluir solo el hash de un bloque en cada votación para ahorrar ancho de banda. Antes de activar el voto por hash, se requería todo el contenido del bloque.</p>

