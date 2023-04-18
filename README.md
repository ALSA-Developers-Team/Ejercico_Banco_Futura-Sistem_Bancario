
# Requerimiento de Implementación de Sistema Bancario para Banco Futura

Estimado desarrollador,

Nos complace informarle que ha sido seleccionado para desarrollar un sistema bancario básico en Java para el Banco Futura. Este sistema debe permitir la gestión de diferentes tipos de cuentas bancarias, como cuentas corrientes y cuentas de ahorro, utilizando conceptos de herencia y polimorfismo.

A continuación, se presenta un resumen de los requisitos y reglas de negocio que deben ser implementados en el sistema:

## Requisitos del sistema

1.  Crear una clase abstracta llamada `CuentaBancaria` que represente una cuenta bancaria genérica. Esta clase debe contener los siguientes atributos: número de cuenta, titular, saldo y fecha de apertura.
    
2.  Implementar los siguientes métodos en la clase `CuentaBancaria`: depositar, retirar y calcular interés. El método calcular interés debe ser abstracto, ya que su implementación variará según el tipo de cuenta.
    
3.  Crear dos clases que hereden de `CuentaBancaria`: `CuentaCorriente` y `CuentaAhorro`. La clase `CuentaCorriente` debe tener un límite de sobregiro y una tasa de interés de sobregiro, mientras que la clase `CuentaAhorro` debe tener una tasa de interés.
    
4.  Sobreescribir el método retirar en la clase `CuentaCorriente` para permitir sobregiros y aplicar la tasa de interés correspondiente en caso de saldo negativo.
    
5.  Implementar el método calcular interés en ambas clases (`CuentaCorriente` y `CuentaAhorro`) según las reglas específicas de cada tipo de cuenta.
    
6.  Crear una clase `Banco` que contenga un listado de cuentas bancarias y métodos para agregar, eliminar y buscar cuentas.
    
7.  Crear una clase principal `Main` donde se instancien objetos de `CuentaCorriente` y `CuentaAhorro`, se utilice polimorfismo para interactuar con ellos y se muestren los resultados de las operaciones realizadas.
    

## Reglas de negocio

### Cuenta Corriente

1.  La cuenta corriente permite a los titulares realizar depósitos, retiros y transferencias.
2.  La cuenta corriente puede tener un saldo negativo hasta un límite predefinido, conocido como límite de sobregiro. Este límite debe ser establecido al momento de crear la cuenta.
3.  Cuando el saldo de la cuenta corriente es negativo, se aplica una tasa de interés de sobregiro sobre el monto sobregirado. Esta tasa de interés debe ser establecida al momento de crear la cuenta.
4.  El banco puede cobrar comisiones por mantenimiento de cuenta, transferencias, uso de cheques, entre otros. Estas comisiones pueden variar según las políticas del banco y deben ser informadas al titular de la cuenta.
5.  La cuenta corriente no genera intereses sobre el saldo positivo.

### Cuenta de Ahorro

1.  La cuenta de ahorro permite a los titulares realizar depósitos y retiros, pero generalmente no permite realizar transferencias directas a otras cuentas.
2.  La cuenta de ahorro no permite tener un saldo negativo. Si se intenta retirar un monto mayor al saldo disponible, la operación debe ser rechazada. 3. La cuenta de ahorro genera intereses sobre el saldo positivo según una tasa de interés predefinida, que debe ser establecida al momento de crear la cuenta.

4.  Los intereses generados en la cuenta de ahorro son capitalizados periódicamente (por ejemplo, mensual o anualmente) y se suman al saldo de la cuenta.
5.  El banco puede cobrar comisiones por mantenimiento de cuenta y retiros en ventanilla, entre otros. Estas comisiones pueden variar según las políticas del banco y deben ser informadas al titular de la cuenta.

## Tasas y cobros sugeridos

| Concepto                          | Cuenta Corriente | Cuenta de Ahorro |
|-----------------------------------|------------------|------------------|
| Tasa de interés de sobregiro     | 12% anual        | N/A              |
| Tasa de interés por saldo positivo| 0%               | 1.5% anual       |
| Comisión por mantenimiento        | $5 mensual       | $2 mensual       |
| Comisión por retiro en ventanilla | $1 por retiro    | $1 por retiro    |
| Comisión por transferencia        | $2 por transferencia | N/A          |
| Comisión por uso de cheques       | $0.50 por cheque | N/A              |


Estos valores son solo ejemplos y pueden variar dependiendo del banco y del país en el que se encuentren. Por favor, utilice estos valores como parámetros iniciales al momento de crear las cuentas corriente y de ahorro en el sistema bancario.

Agradecemos su atención a estos requerimientos y estamos ansiosos de ver el resultado de su trabajo en nuestro nuevo sistema bancario para el Banco Futura. Por favor, no dude en ponerse en contacto con nosotros si necesita aclaraciones adicionales o si tiene alguna pregunta sobre los requerimientos.

Atentamente,

ALSA DevTeam

Representantes del desarrollo en Banco Futura

Banco Futura
