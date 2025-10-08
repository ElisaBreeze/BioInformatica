

# Del ADN a la Proteína

## Elisa Breeze y Néstor Ortega

## Bioinformática

### 6 Octubre 2025


 En la carpeta se puede encontrar lo siguiente:  
 - Un pdf con el informe de los ejercicios resueltos  
 - El apoyo visual para la presentación  
 - El código de los ejercicios resueltos  
 - Dos ficheros de datos usados en la resolución de datos  

   
## Ejercicio 1: Replicación del ADN

**Objetivo** : comprender el mecanismo semiconservativo y las enzimas implicadas.
**Instrucciones** :

**1.** Considera la siguiente secuencia de ADN: 5’ – ATG CCG TTA GCT – 3’ / 3’ – TAC GGC
AAT CGA – 5’.  
**2.** Realiza una ronda de replicación:  

 - Identifica las nuevas hebras que se formarán.  
       **Molécula original:**  
       5’ – ATGCCGTTAGCT – 3’ (vieja)  
       3’ – TACGGCAATCGA – 5’ (vieja)  
       **Después de la replicación (una ronda):**  
       **Dúplex 1:**  
       5’ – ATGCCGTTAGCT – 3’ (vieja)  
       3’ – TACGGCAATCGA – 5’ (nueva)  
       **Dúplex 2:**  
       5’ – ATGCCGTTAGCT – 3’ (nueva)  
       3’ – TACGGCAATCGA – 5’ (vieja)  


- Indica cuál sería la función de las enzimas helicasa, primasa, ADN polimerasa y
       ligasa en este proceso.  
       **Helicasa** : Separa las hebras, es decir, desenrolla la doble hélice  
       **Primasa** : Sintetiza pequeños fragmentos de ARN que sirven como cebadores
       permitiendo que inicien la síntesis de nuevas hebras complementarias. Es decir, da
       un punto de inicio a la ADN polimerasa.  
       **ADN polimerasa:** Añade nucleótidos complementarios a la hebra molde.  
       **Ligasa** : Une los fragmentos de ADN sintetizados  


**3**. Reflexiona: ¿qué ocurriría si la ADN polimerasa cometiera un error en una base y no se
corrigiera?  
  
  
Si la ADN polimeras cometiera un error en una base y no se corrigiera, se convertiría en una
mutación, porque la hebra nueva tendría una base errónea, y en la replicación siguiente se
copiará el error, causando una mutación, pudiendo afectar toda la descendencia si no se
corrige, volviéndose permanente.
  
  
**Extensión con Biopython:**  
Escribe un pequeño script que, dada una cadena de ADN, genere automáticamente su
hebra complementaria, y comprueba si tu resultado coincide con lo que obtuviste
manualmente.  
  
**La respuesta a esta parte del ejercicio se encuentra en el archivo codigoEjercicios.ipynb**  
  
## Ejercicio 2: Transcripción del ADN a ARN  
  
**Objetivo:** traducir correctamente la información de la cadena molde.  
**Instrucciones**:  

**1.** Usa la siguiente secuencia de ADN: 5’ – ATG CCT GAA TGC – 3’ / 3’ – TAC GGA CTT
ACG – 5’.    
**2**. Identifica cuál es la cadena molde.  
La hebra molde va de 3’ a 5’, por lo que sería: 3’ – TAC GGA CTT ACG –5’  
**3.** Obtén el transcrito de ARN correspondiente (recuerda que el ARN se sintetiza en
dirección 5’ → 3’ y utiliza uracilo en lugar de timina).  
  
El transcrito de ARN correspondiente sería: 5’- AUG CCU GAA UGC-3’  
  
**4.** Explica cuál sería la región promotora y cuál la región codificante.  
  
Región promotora se suele encontrar en el extremo 5’ de la cadena codificante, sirve como
sitio de unión para la ARN polimerasa y para los factores de transcripción. En este caso no
se ve ninguna región promotora. La región codificante por otro lado, es la parte del ADN que
se transcribe a ARNm y luego se puede traducir en proteína.  
  
La **región promotora:** En este caso no hay región promotora  
La **región codificante** sería: 5’ – ATG CCT GAA TGC – 3  
  
  
**Extensión con Biopython:**  
Crea un script que lea un archivo FASTA con ADN y produzca la secuencia de ARNm.
Experimenta cambiando la orientación de la hebra y observa qué ocurre.  
  
**La respuesta a esta parte del ejercicio se encuentra en el archivo codigoEjercicios.ipynb**    
  
Se observa que las dos secuencias de ARNm resultantes son completamente distintas, lo
cual nos muestra que la direccionalidad 5’→3’ y la hebra molde correcta son esenciales en
la transcripción genética, porque cambiar la orientación de la hebra implica transcribir una
cadena distinta, que no produce el mismo ARNm ni codifica la misma proteína.  
  
## Ejercicio 3. Traducción del ARNm a proteína  
  
**Objetivo** : aplicar el código genético y reflexionar sobre mutaciones.  
**Instrucciones:**   

**1.** Usa el siguiente transcrito de ARN: 5’ – AUG UAU GCU UAA – 3’.  
**2**. Identifica el codón de inicio y el codón de paro.  
  
Inicio **: AUG** → Metionina (Met) y señal de inicio.  
Paro **: UAA** → codón STOP (no codifica aminoácido). 
  
**3.** Traduce la secuencia en una cadena de aminoácidos.  
  
AUG → **Met** (Metionina)  
UAU → **Tyr** (Tirosina)  
GCU → **Ala** (Alanina)  
UAA → **STOP** (Codón de terminación, no codifica aminoácido)  
  
**Proteína resultante:** Met – Tyr – Ala  
**Abreviatura** : MYA  
  
**4.** Reflexiona: ¿qué pasaría si el codón de inicio mutara de AUG a GUG? ¿Qué ocurriría si
el codón de paro desapareciera por mutación?  
  
- **AUG → GUG (inicio mutado):** normalmente no inicia la traducción (AUG es la señal
       estándar). En algunos sistemas GUG puede iniciar con menor eficiencia; podría no
       producirse la proteína o producirse muy poco.  
- **Desaparece el STOP (UAA muta):** la traducción continúa hasta el siguiente STOP
       aguas abajo → proteína más larga (extendida), con riesgo de pérdida de función,
       mal plegamiento o toxicidad.  
  
**Extensión con Biopython:**  
Utiliza el módulo Bio.Seq para traducir automáticamente el ARNm a una secuencia proteica
y comprueba si el resultado coincide con el tuyo.   
  
**La respuesta a esta parte del ejercicio se encuentra en el archivo codigoEjercicios.ipynb**   
  
## Ejercicio 4. Splicing alternativo  
  
**Objetivo** : comprender cómo un mismo gen puede generar varias proteínas.  
**Instrucciones:  
1**. Considera un gen con 5 exones: Exón 1 – Exón 2 – Exón 3 – Exón 4 – Exón 5.  
  
#### 2. Diseña al menos dos combinaciones de splicing alternativo (por ejemplo, 1-2-4-5 o 1-3-5).  

**Isoforma A (1–2–3–5)**  
● Se omite el **Exón 4** (la parte catalítica).  
● La proteína resultante no tiene actividad enzimática, pero aún puede unirse a otras
proteínas gracias a los exones 2 y 3.  
● Podría actuar como proteína reguladora o inhibidora, bloqueando la acción de otras
isoformas.  
**Isoforma B (1–2–4–5)**  
● Se elimina el **Exón 3** (regulador).  
● Mantiene la parte catalítica (Exón 4), por lo que es activa.  
● Sin el dominio regulador, podría ser más activa o menos controlada, aumentando la
actividad enzimática.  
  
**3**. Explica qué diferencias esperarías en las proteínas resultantes.  
  
La **isoforma A** (1–2–3–5) pierde el exón 4, por lo que no tiene actividad enzimática, aunque
puede unirse a otras proteínas y actuar como reguladora. En cambio, la **isoforma B**
(1–2–4–5) conserva el exón 4 (la parte activa), pero pierde el exón 3, que servía para
controlar la actividad. Así, la isoforma A es inactiva pero reguladora, mientras que la B es
activa pero menos controlada.  
  
**4.** Reflexiona: ¿por qué este mecanismo aumenta la diversidad proteica sin necesidad de
más genes?  
  
El splicing alternativo permite que un solo gen genere múltiples ARNm (y por tanto varias
proteínas distintas). No hace falta más genes; basta con reordenar o excluir exones durante
el procesamiento del ARN.  
  
  
**Extensión con Biopython / bases de datos:**    
Busca en Ensembl un gen humano conocido con isoformas (por ejemplo, FGFR2) y
compara sus diferentes transcritos. Reflexiona sobre cómo estas diferencias podrían afectar
a la función de la proteína.  
  
  
**La respuesta a esta parte del ejercicio se encuentra en el archivo codigoEjercicios.ipynb**  
  
Se compararon las isoformas **FGFR2-206, -203 y -210**. Las comparaciones a nivel de
**nucleótidos** muestran que las isoformas **FGFR2-206** y **FGFR2-203** presentan una
identidad muy alta (99.76 %), lo que indica que solo difieren en pequeños fragmentos de la
secuencia —probablemente por la inclusión o exclusión de un exón corto—, manteniendo
así casi la misma información genética. En cambio, la isoforma **FGFR2-210** muestra una identidad menor (alrededor del 90 %) y una longitud más corta, lo que sugiere la pérdida de uno o varios exones que podrían codificar regiones funcionales importantes.
A nivel de **proteína** , las diferencias siguen el mismo patrón: FGFR2-206 y FGFR2-203 son
prácticamente idénticas (99.76 % de identidad, 821 y 819 aminoácidos), mientras que
FGFR2-210 es más corta (768 aminoácidos) y conserva solo un 90 % de similitud. Estas
variaciones estructurales indican que, aunque las tres isoformas derivan del mismo gen,
**FGFR2-210 probablemente tiene una función distinta** , debida a la alteración o pérdida de
dominios proteicos implicados en la unión a ligandos o en la señalización celular.  
  
## Ejercicio 5. Introducción a las proteínas  
  
**Objetivo** : relacionar secuencia, estructura y función.  
Instrucciones:  
  
**1.** Considera la siguiente secuencia de aminoácidos: Met – Ile – Ser – Gly – Val – Lys – His.  
**2.** Identifica el extremo N y el extremo C de la cadena.  
**Extremo N** : Primer aminoácido de la cadena.  
Primer aminoácido: Met  
**Extremo C:** El último ácido de la cadena.  
Último aminoácido => His  
  
  
**3.** Reflexiona: ¿cómo influye el orden de los aminoácidos en la estructura final de la
proteína? ¿Qué ocurriría si hubiera una mutación que cambiara un aminoácido hidrofóbico
por uno hidrofílico en una región interna de la proteína?  
  
El orden es muy importante, ya que determina cómo se pliega y determina la función de la
proteína. Cada aminoácido tiene propiedades químicas específicas y estas determinan el
modo en el que se pliega la cadena. Esto a su vez define la estructura final y la función. Si
hay una mutación que cambia un aminoácido hidrofóbico (repelente al agua) por uno
hidrofílico (atraído por el agua) en una región interna de la proteína, podría desestabilizarse
el núcleo y llevar a que no se pliegue correctamente, pudiendo afectar su función, e incluso
llevar a que se agregue a otras proteínas o degrade.  
  
  
**Extensión con Bioinformática:**  
Busca en el Protein Data Bank (PDB) la estructura de una proteína conocida y observa
cómo los aminoácidos se organizan en hélices alfa y láminas beta. Reflexiona sobre cómo
una mutación puntual podría afectar al plegamiento:  
  
  
La lisozima es una proteína que daña las paredes celulares de las bacterias, actuando así
como una barrera natural contra infecciones.
En la imagen (Visualizadble en el PDF BIOPA2.pdf) se puede observar su estructura, donde las hélices alfa son las partes
enrolladas en forma de muelle, y las láminas beta son las partes más planas y extendidas.
Las partes que parecen ganchos, son puentes disulfuro, que se encargan de mantener la
forma estable.  
  
Si se cambia un aminoácido, puede tener un efecto importante, pudiendo perderse la
estabilidad e incluso llegar a deformarse si se cambia un aminoácido que forma un puente
disulfuro. Por otro lado, si se cambian otros aminoácidos podría llegar a deshacerse,
romperse o incluso afectar las interacciones con otras partes o con el entorno. En
conclusión, una pequeña mutación podría afectar gravemente cómo se pliega, pudiendo
cambiar su forma, haciéndola menos estable y que no funcione correctamente.  
  
## Ejercicio 6. Actividad integradora: del ADN a la proteína  
  
**Objetivo** : recorrer el dogma central completo.  
**Instrucciones:**  
  
**1.** Escoge una secuencia de ADN (codificada en un fichero fasta de algún banco de datos o
página especializada públicos).  
**2.** Paso 1: Replica la secuencia indicando las dos nuevas hebras.  
**3**. Paso 2: Transcribe la cadena molde en ARNm.  
**4.** Paso 3: Traduce el ARNm en una cadena de aminoácidos.  
  
**5**. Reflexiona: ¿qué punto del proceso es más vulnerable a errores que afecten a la función
de la proteína?  
  
El punto del proceso más vulnerable es la traducción, dado que es cuando se determina la
secuencia de aminoácidos que forma la proteína, y si hay un error en este paso, se podría
alterar su estructura, y por ende su función biológica también. Además de ello, la replicación
también es muy importante porque cualquier error ocurrido en este paso se puede transmitir
a las células hijas. Por otro lado, los errores durante la transcripción son menos
impactantes, ya que los ARNm defectuosos no se heredan.  
  
  
**6**. Programa un pipeline que realice los tres procesos (replicación, transcripción, y
traducción.  
  
**La respuesta a esta parte del ejercicio se encuentra en el archivo codigoEjercicios.ipynb**  
  
  
**Extensión con Biopython:**  
El pipeline que realice los tres pasos: generar la hebra complementaria (replicación),
obtener el transcrito (transcripción) y traducir a proteína (traducción) debe informar en todo
momento de lo que está ocurriendo en los procesos.  
  
**La respuesta a esta parte del ejercicio se encuentra en el archivo codigoEjercicios.ipynb**  
