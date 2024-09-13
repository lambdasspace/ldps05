## Lenguajes de Programación
### Evaluación Semanal 5

#### 📝 Instrucciones

- El semanal podrá resolverse **en equipos de 3**.
- Se deberá entregar por medio de GitHub Classroom a más tardar a las **23:59:59 del miércoles 18 de septiembre de 2024**. **No habrán prórrogas**. En caso de requerir más tiempo, se descontará un punto por cada día de entrega tardío.
- Cualquier duda podrá extenarse en la clase, por correo o por medio de Telegram en un horario de 9:00 a 18:00.
- Deberá entregarse en formato LaTeX.
- No es necesario que vuelvan a escribir los ejercicios completos, basta con que los numeren y entreguen **en orden**.

#### 🚀 Ejercicios

1. Convertir la siguiente expresión a su respectiva versión usando índices de *De Bruijn*.

   ```lisp
   (let (a 2)
      (let (b 3)
         (let (c 4)
            (let (d (+ a (- b c)))
               (let (f (let (a (+ b c)) a))
                  (+ d (let (b (- d f)) (- b c))))))))
   ```


2. Dada la siguiente expresión representada mediante índices de *De Bruijn*, obtener su respectiva versión usando indentificadores de variables.

   ```lisp
   (let (+ 2 3)
      (let 17
         (let (+ <:0> <:0>)
            (let (- <:0> (+ <:1> <:2>))
               (let (let 2 (+ <:0> 3))
                  (- <:3> (+ <:2> (+ <:0> <:1>))))))))
   ```

3. Aplicar las β-reducciones correspondientes a las siguientes expresiones hasta llegar a una forma Normal o justificar por qué dicha forma no existe. Indicar en cada paso la *redex* y el *reducto*. Considerar las siguientes definiciones

   - *I =def λx.x*
   - *K =def λx.λy.x*
   - *S =def λx.λy.λz.xy(yz)*
   - *Ω =def (λx.xx)(λx.xx)*

   (a) *λx.xKΩ*   
   (b) *(λx.x(II))z*   
   (c) *(λu.λv.(λw.w(λx.xu))v)y(λz.λy.zy)*   
   (d) *S(KI)(KI)*   

4. De acuerdo a la representación de números (Numerales de Church) y representación de booleanos en el Cálculo λ:

   (a) Definir la función *<* que decide si un número es menor a otro.   
   (b) Definir la función *↔* (bicondicional) sobre booleanos.   
   (c) Definir la función disunción exclusiva *or* sobre booleanos.