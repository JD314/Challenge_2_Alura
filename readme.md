# 📊 Informe de Evasión de Clientes (Churn)

## 1. Introducción

El presente análisis tiene como objetivo identificar patrones y factores relacionados con la **evasión de clientes** en una empresa de telecomunicaciones. Este fenómeno, conocido como *churn*, representa una pérdida significativa para el negocio, por lo que comprender sus causas es clave para implementar estrategias de retención efectivas.

---

## 2. Limpieza y Tratamiento de Datos

- Se integraron varias secciones del JSON (`customer`, `phone`, `internet`, `account`) en un único DataFrame.
- Se convirtieron columnas categóricas binarias (`Yes`/`No`) a formato numérico (1/0).
- Se eliminaron inconsistencias y se convirtieron los campos numéricos (como `Charges.Total`) a tipo `float`.
- Se creó una nueva columna `Charges.daily` como estimación del costo diario del servicio.

---

## 3. Análisis Exploratorio de Datos (EDA)

Se compararon clientes retenidos (`Churn = 0`) y perdidos (`Churn = 1`) mediante visualizaciones.

### Distribución de Cargos

- Los clientes perdidos tienden a tener menores cargos totales acumulados.
- En cargos mensuales, los clientes perdidos están más concentrados en valores intermedios-altos.



---

### Tenencia, Contrato y Tipo de Internet

- Los clientes que abandonan el servicio suelen tener **poca antigüedad** (tenure bajo).
- La **modalidad "Month-to-month"** está fuertemente asociada al churn.
- **Internet por fibra óptica** es más común entre los clientes que se dan de baja.



---

## 4. Conclusiones e Insights

- La mayoría de los clientes que se van tienen:
  - Menos de 12 meses en la empresa.
  - Contrato mes a mes.
  - Servicio de internet por fibra.
- Hay un **grupo vulnerable al churn** claramente identificable por estos patrones.
- **El churn parece relacionado con la falta de fidelización temprana.**

---

## 5. Recomendaciones

- Implementar **bonificaciones de permanencia** para nuevos clientes (primeros 12 meses).
- Ofrecer **descuentos o planes anuales** que compitan con la modalidad "Month-to-month".
- Analizar la calidad del servicio de **internet por fibra óptica**, dado su vínculo con el churn.
- Utilizar estos perfiles para **detectar clientes en riesgo** y anticiparse al abandono.