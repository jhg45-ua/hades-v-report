# Proyecto HaDes-V: Memoria Técnica y Resultados

Bienvenido a la documentación oficial del procesador **HaDes-V**, un microcontrolador basado en la arquitectura de conjunto de instrucciones **RISC-V (RV32I)**, sintetizado e implementado físicamente sobre la FPGA Xilinx Artix-7 (Nexys A7-100T).

!!! info "Descargar Memoria Técnica Oficial (PDF)"
    :material-file-pdf-box: **[Descargar Informe Técnico de HaDes-V](assets/HaDes_V_Informe_Tecnico.pdf)**

---

## Resumen de Hitos Arquitectónicos

1. **Especulación de Control:** Predictor dinámico de saltos *Branch History Table* (BHT) de 1024 entradas con contadores saturantes de 2 bits y *JAL Bypass* en Fetch.
2. **Jerarquía de Memoria L1:** Cachés Harvard independientes de instrucciones (I-Cache) y datos (D-Cache) de mapeo directo, complementadas con *Write Buffer* asíncrono.
3. **Cierre Físico de Tiempos:** Operación a **100 MHz** con *Slack* temporal positivo (**WNS: +0.036 ns**).
4. **Telemetría Hardware:** Inserción de Contadores de Rendimiento de Hardware (*HPCs*) en la etapa de Writeback.