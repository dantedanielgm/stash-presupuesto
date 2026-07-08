# 💸 Stash — presupuesto 20/50/30 para ingresos irregulares

**Una app de presupuesto por sobres, hecha para quien cobra por quincenas, arrastra deudas y vive la plata de verdad — no la del Excel perfecto.**

🔗 **Ábrela ahora:** **[dantedanielgm.github.io/stash-presupuesto](https://dantedanielgm.github.io/stash-presupuesto/)**

Sin cuenta, sin instalar, sin costo. Funciona en el celular y en la compu. Tus datos nunca salen de tu dispositivo.

---

## Por qué existe

Los presupuestos tradicionales asumen un sueldo fijo el día 30 y cero deudas. La vida real de mucha gente no es así: te pagan por partes, tienes tarjetas revolviendo al 165% de interés, y a veces el sueldo aún no cae cuando ya estás planificando.

Stash nace de una idea vieja y simple —**"págate a ti primero"**— y la vuelve ejecutable. Por eso la regla no es 50/30/20 sino **20/50/30**: el 20 de ahorro va **primero**, no con lo que sobra.

| | |
|---|---|
| 🟢 **20% Ahorro** | Todo sol que sube tu patrimonio: pagar deuda, colchón, metas, invertir. |
| 🔵 **50% Necesidades** | Techo, comida, transporte, salud, educación. |
| 🟡 **30% Gustos** | Lo que hace que la vida valga la pena vivirla. |

---

## Qué lo hace distinto

- **📅 Quincena nativa.** No es un presupuesto mensual parchado. Cada ciclo (quincena, mes o periodo libre) es un estado de cuenta propio: abres con X, te mueves, cierras con Y.
- **💳 Deuda revolvente de primera clase.** Modela tarjetas como lo que son (línea, disponible, mínimo, TCEA) y te dice la verdad incómoda: a 165% de interés, tarjetear es trampa, no puente. Prioriza qué pagar primero (bola de nieve).
- **🌊 Cascada automática.** Si te pasas en una caja, el sobrante se cubre solo desde donde hay saldo — sin que hagas la resta a mano. Nunca ves un número negativo que no puedas administrar.
- **💰 Contador vivo bidireccional.** "Dinero que tienes ahora" baja con cada gasto que marcas ✓ y sube cuando marcas que te llegó un ingreso. Lo que aún no cae se ve como *por llegar*, no como un rojo mentiroso.
- **⚡ Gasto suelto en 2 taps.** Botón flotante → monto → listo. Se anota y baja de tu plata al instante.
- **🔒 Reserva honesta.** Cuando marcas ahorro, la app pregunta claro: *¿se pagó o quedó en tu Reserva?* Cada sol sabe a dónde fue.
- **🌎 Gratis, en español, sin cuenta.** Un link que compartes por WhatsApp. Tu familia lo abre y lo usa.

---

## Cómo se usa

1. **Abre el link** → [dantedanielgm.github.io/stash-presupuesto](https://dantedanielgm.github.io/stash-presupuesto/)
2. Responde el onboarding corto (¿cómo te pagan? ¿tienes algo ahorrado?).
3. Reparte tu quincena en las 3 cajas, agrega tus deudas, marca lo que pagas.
4. Al terminar el ciclo, **ciérralo** y la app pasa a la siguiente quincena.

### Instalar como app (opcional)
En el celular: abre el link → menú del navegador → **"Agregar a pantalla de inicio"**. Queda como una app nativa, funciona offline.

### Mover tus datos entre dispositivos
Los datos viven **solo en tu navegador** (no hay servidor). Para pasarlos de un aparato a otro: **⬇ Exportar copia** en uno → **⬆ Importar copia** en el otro. Esa copia también es tu red de seguridad.

---

## Privacidad

**Cero backend. Cero cuentas. Cero telemetría.** Todo se guarda en el `localStorage` de tu propio navegador. Nadie —ni yo— ve tus números. Si borras los datos del navegador, se van; por eso existe Exportar/Importar.

---

## Cómo está hecho

Stash es **un solo archivo HTML** (`index.html`) con todo adentro: estructura, estilos y lógica. Sin frameworks, sin build de JavaScript, sin dependencias externas.

- **Principio rector — "la telaraña":** una sola fuente de verdad + estado derivado. Mover una cosa mueve todo (full re-render reactivo). No hay dos números que puedan desincronizarse.
- **PWA:** `manifest.webmanifest` + `sw.js` (service worker) para que funcione offline e instalable.
- **Persistencia:** `localStorage`, con Exportar/Importar en JSON.

### Desarrollo local

La fuente de verdad es **`presupuesto.html`** (en la carpeta de trabajo). La carpeta `web/` que ves en este repo es **derivada** — se regenera, no se edita a mano:

```powershell
# 1. Editas presupuesto.html
# 2. Regeneras la carpeta de despliegue:
.\build-pwa.ps1
# 3. Publicas el contenido de web/ (GitHub Pages lo sirve solo)
```

Para probar en local, basta abrir `presupuesto.html` en el navegador (o servirlo con cualquier server estático). No necesita instalación de nada.

---

## Estado

**Beta viva (julio 2026).** El núcleo es sólido y se usa a diario con datos reales. Sigue evolucionando por uso: cada fricción que aparece en la calle se arregla y se vuelve a publicar en el mismo link.

**Roadmap abierto:** cadencia de gastos recurrentes, historial de cierres (patrimonio neto por ciclo), simulador de interés compuesto ampliado, y afinar el modelo de tarjeta con el interés real.

---

## Autor

Hecho por **Dante Daniel Gutiérrez Matos** ([@dantedanielgm](https://github.com/dantedanielgm)) — construido de forma conversacional con Claude Code, iterando sobre problemas reales de presupuesto quincenal.

## Licencia

Código abierto para uso personal. Si quieres reutilizarlo o adaptarlo, adelante — un crédito se agradece.
