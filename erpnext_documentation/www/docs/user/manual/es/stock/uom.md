<!-- add-breadcrumbs -->
# Unidad de Medida (UOM)

**Una UOM es una unidad que se utiliza para medir los Productos.**

Hay muchas UOM creadas de forma predeterminada en ERPNext. Sin embargo, pueden añadirse más de acuerdo con las necesidades del negocio que las utilice.  
En las UOM hay una opción "Debe ser un número entero". Si esta opción está tildada, no se pueden utilizar fracciones en esta UOM. Para saber más respecto a fracciones y UOMs ver [esta página](/docs/user/manual/es/stock/articles/managing-fractions-in-uom).

La lista de UOM en sí misma solo guarda el nombre. Las tasas de conversión son almacenadas en un documento llamado "Factor de Conversión de UOM". Si se suman nuevas UOMs y se piensa utilizarlas en transacciones donde deberán convertirse en otras UOMs, es aconsejable que se las añada a esta lista.

Por ejemplo, aquí 1 Kilo es aproximadamente 2,2 Libras y el factor de conversión exacto es almacenado: 

![UoM conversion factor](/docs/assets/img/stock/uom_convert.png)
