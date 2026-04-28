# Sintaxis básica de Markdown

Este documento muestra **los elementos más usados de Markdown** con una breve explicación y un ejemplo de cada uno.

---

# 1. Cabeceras

Los encabezados en Markdown se crean utilizando el símbolo #. La cantidad de símbolos # antes del texto determinará el nivel del encabezado, con # siendo el más grande (equivalente a \<h1\> en HTML) y ###### el más pequeño (equivalente a \<h6\>). Aquí tienes un ejemplo de cómo se utilizan:

```markdown
# Cabecera nivel 1
## Cabecera nivel 2
### Cabecera nivel 3
#### Cabecera nivel 4
##### Cabecera nivel 5
###### Cabecera nivel 6
Cabecera nivel 1 (Usando =)
=====
Cabecera nivel 2 (Usando -)
-----
```

**Resultado**:

# Cabecera nivel 1

## Cabecera nivel 2

### Cabecera nivel 3

#### Cabecera nivel 4

##### Cabecera nivel 5

###### Cabecera nivel 6

Cabecera nivel 1 (Usando =)
====

Cabecera nivel 2 (Usando -)
----

---

# 2. Párrafos y saltos de línea

Para crear un párrafo, simplemente escribe texto separado por una línea en blanco.  
Si quiero que haya un salto entre frases, pero sin línea en blanco , debo poner **dos espacios** al final de la primera frase 

```markdown
Este es el primer párrafo.

Este es el segundo párrafo.

Esto es el tercer párrafo.
Pero ahora no salto de línea.

Esto es el cuarto párrafo.  
Pero ahora salto de línea.
```

**Resultado**:

Este es el primer párrafo.

Este es el segundo párrafo.

Esto es el tercer párrafo.
Pero ahora no hay salto de línea.

Esto es el cuarto párrafo.  
Pero ahora salto de línea.

---

# 3. Texto en negrita, cursiva y tachado

```markdown
**Texto en negrita**
__Texto en negrita__
*Texto en cursiva*
_Texto en cursiva_  
***Texto en negrita y cursiva***
~~Texto tachado~~
```

**Resultado**:

**Texto en negrita**

__Texto en negrita__

*Texto en cursiva*

_Texto en cursiva_

***Texto en negrita y cursiva***

~~Texto tachado~~

---

# 4. Listas no ordenadas

Se crean con `-`, `*` o `+`.

```markdown
- Elemento 1
* Elemento 2
+ Elemento 3

- Elemento de lista 1
- Elemento de lista 2
    - Elemento de lista 3
    - Elemento de lista 4
        - Elemento de lista 5
        - Elemento de lista 6
```

**Resultado**:

- Elemento 1
* Elemento 2
+ Elemento 3

**Resultado listas anidadas**:

- Elemento de lista 1
- Elemento de lista 2
    - Elemento de lista 3
    - Elemento de lista 4
        - Elemento de lista 5
        - Elemento de lista 6

---

# 5. Listas ordenadas

Se crean con números seguidos de punto.

```markdown
1. Elemento de lista 1
2.  Elemento de lista 2
    - Elemento de lista 3
    - Elemento de lista 4
        1. Elemento de lista 5
        2. Elemento de lista 6
```

**Resultado**:

1. Elemento de lista 1
2.  Elemento de lista 2
    - Elemento de lista 3
    - Elemento de lista 4
        1. Elemento de lista 5
        2. Elemento de lista 6
---

# 6. Listas anidadas

Permiten crear subniveles.

```markdown
- Lenguaje
  - Java
  - Python
  - C#
```

**Resultado**:

* Lenguajes

  * Java
  * Python
  * C#

---

# 7. Enlaces

Se crean con el texto entre corchetes y la URL entre paréntesis.

```markdown
La empresa [OpenAI](https://openai.com) desarrolla ChatGPT

Haz click para ir a [Markdown.es](https://markdown.es/)
```

***Resultado***:

La empresa [OpenAI](https://openai.com) desarrolla ChatGPT

Haz click para ir a [Markdown.es](https://markdown.es/)

## 7.1 Enlaces automáticos
Cuando quieres ver la url completa.

```markdown
La empresa <https://openai.com> desarrolla ChatGPT

Haz click para ir a <https://markdown.es/>
```

***Resultado***:

La empresa <https://openai.com> desarrolla ChatGPT

Haz click para ir a <https://markdown.es/>

## 7.2 Enlaces por referencia

```markdown
[EnlceOpenAI]: https://openai.com

[EnlaceMarkdown.es]: https://markdown.es

La empresa [OpenAI][EnlceOpenAI] desarrolla ChatGPT

Haz click para ir a [Markdown][EnlaceMarkdown]
```

**Resultado enlces por refetrencia**:

[EnlceOpenAI]: https://openai.com

[EnlaceMarkdown]: https://markdown.es

La empresa [OpenAI][EnlceOpenAI] desarrolla ChatGPT

Haz click para ir a [Markdown][EnlaceMarkdown]

---

# 8. Imágenes

La sintaxis es similar a los enlaces, pero añadiendo `!`.  
Title de la imagen (opcional): podemos añadir un "title" a la imagen, que se verá cuando pase el ratón sobre ella añadiendo entre comillas un texto justo detrás del enlace de la imagen.

```markdown
![Imagen CSS3 (Texto alternativo)](https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg)

![Imagen Montaña (Texto alternativo)](img/raghavdduck-mountain-10205639.jpg)

![Imagen CSS3 (Texto alternativo)](https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg  "Title imagen - Logo CSS3")

![Imagen Montaña (Texto alternativo)](img/raghavdduck-mountain-10205639.jpg  "Title - Montaña")
```

**Resultado**:

![Imagen CSS3 (Texto alternativo)](https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg)

![Imagen Montaña (Texto alternativo)](img/raghavdduck-mountain-10205639.jpg)

![Imagen CSS3 (Texto alternativo)](https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg  "Title imagen - Logo CSS3")

![Imagen Montaña (Texto alternativo)](img/raghavdduck-mountain-10205639.jpg  "Title - Montaña")

## 8.1 Enlaces por referencia a imágenes

Ya que al añadir imágenes también estás tratando con URLs, puedes utilizar el método que viste anteriormente para incluir links mediante referencias, solo que en este caso los enlaces de referencia serán aquellos donde se encuentre tu imagen.

```markdown
![img1]: https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg  "Title imagen - Logo CSS3"

![img2]: img/raghavdduck-mountain-10205639.jpg  "Title - Montaña"

![Texto alternativo img1][img1]

![Texto alternativo img2][img2]
```

**Resultado enlces de imágenes**:

[img1]: https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg  "Title imagen - Logo CSS3"

[img2]: img/raghavdduck-mountain-10205639.jpg  "Title - Montaña"

![Texto alternativo img1][img1]

![Texto alternativo img2][img2]

---

# 9. Citas

Se crean con `>`.

```markdown
> Esto es una cita.

> Un país, una civilización se puede juzgar por la forma en que trata a sus animales.  — Mahatma Gandhi

> Esto sería una cita como la que acabas de ver.
> 
> > Dentro de ella puedes anidar otra cita.
> 
> La cita principal llegaría hasta aquí. 
```

**Resultado**:

> Esto es una cita.

> Un país, una civilización se puede juzgar por la forma en que trata a sus animales.  — Mahatma Gandhi

**Resultado**:

> Esto sería una cita como la que acabas de ver.
> 
> > Dentro de ella puedes anidar otra cita.
> 
> La cita principal llegaría hasta aquí. 

# 10. Bloques de texto

Si quieres crear un bloque entero que contenga código. Lo único que tienes que hacer es encerrar dicho párrafo entre dos líneas formadas por tres \~ virgulillas (Alt + 126 en el teclado numérico).

```markdown
~~~
Creando códigos de bloque.
Puedes añadir tantas líneas y párrafos como quieras.  
~~~
```

**Resultado**:


~~~
Creando códigos de bloque.
Puedes añadir tantas líneas y párrafos como quieras.  
~~~

---

# 11. Código en línea

Se usa una sola comilla invertida.  
Tambiém puedes usar cuatro espacios al principio de cada línea de código (texto preformateado \<pre\>).

```markdown
El comando `print()` muestra información.

     System.out.println("Hola Mundo");
```

**Resultado**:

El comando `print()` muestra información.

     System.out.println("Hola Mundo");

---

# 12. Bloques de código

Se usan tres comillas invertidas.

````markdown
```python
print("Hola mundo")
```
````

**Resultado python**:

```python
print("Hola mundo")
```

````markdown
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

**Resultado json**:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

---

# 13. Tablas

Se crean usando `|` para separar columnas.

```markdown
| Nombre | Edad | Ciudad |
|---------|------|---------|
| Ana     | 20   | Madrid  |
| Luis    | 25   | Murcia  |
```

**Resultado**:

| Nombre | Edad | Ciudad |
| ------ | ---- | ------ |
| Ana    | 20   | Madrid |
| Luis   | 25   | Murcia |

---

# 14. Líneas horizontales

Se crean con tres guiones.

```markdown
línea con guión
---
línea con asterisco
***
línea con subrayado
___
```

**Resultado**:

línea con guión

---

línea con asterisco

***

línea con subrayado

___

# 15. Listas de tareas

Muy usadas en GitHub.

```markdown
- [x] Terminar práctica
- [ ] Subir archivo
```

**Resultado**:

* [x] Terminar práctica
* [ ] Subir archivo

---

# 16. Caracteres escapados

Permiten mostrar símbolos reservados.

```markdown
\*Esto no será cursiva\*
\  barra invertida
`  acento invertido
*  asterisco
_  guión bajo
{} llaves
[] corchetes
() paréntesis
#  almohadilla
+  símbolo de suma
-  guión
.  punto
!  exclamación
```

**Resultado**:

*Esto no será cursiva*  
\\  barra invertida  
\`  acento invertido  
\*  asterisco  
\_  guión bajo  
\{\} llaves  
\[\] corchetes  
\(\) paréntesis  
\#  almohadilla  
\+  símbolo de suma  
\-  guión  
\.  punto  
\!  exclamación
---

# 17. Extensiones de Markdown personalizadas

Ver estas funciones en: [Markdown Adobe](https://experienceleague.adobe.com/es/docs/contributor/contributor-guide/writing-essentials/markdown)

## 17.1 Bloques de notas
Puede elegir entre estos tipos de bloques de notas para llamar la atención sobre un contenido específico:

[!NOTE]  
[!TIP]  
[!IMPORTANT]  
[!CAUTION]  
[!WARNING]  
[!ADMINISTRATION]  
[!AVAILABILITY]  
[!PREREQUISITES] 
[!ERROR]  
[!ADMINISTRATION]  
[!INFO]  
[!SUCCESS]  

En general, los bloques de notas deben usarse con moderación porque pueden resultar molestos. Aunque también se admiten bloques de código, imágenes, listas y vínculos, intente que los bloques de notas sean simples y directos.

```markdown 
>[!NOTE]
>
>This is a standard NOTE block.
CopyToggle Text Wrapping
```

>[!NOTE]
>
>This is a standard NOTE block.
CopyToggle Text Wrapping

```markdown
>[!TIP]
>
>This is a standard TIP.
CopyToggle Text Wrapping
```

>[!TIP]
>
>This is a standard TIP.
CopyToggle Text Wrapping

```markdown
>[!IMPORTANT]
>
>This is an IMPORTANT note.
```
>[!IMPORTANT]
>
>This is an IMPORTANT note.

Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.


