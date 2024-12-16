# Modelo Predictivo para Estimar Tiempos de Entrega de Pedidos

Este proyecto desarrolla un modelo predictivo para estimar el tiempo total necesario para completar pedidos, utilizando datos históricos de órdenes, información de productos, detalles de los shoppers y características de las sucursales.

## Objetivos del Proyecto

### Objetivo General
Desarrollar un modelo predictivo para estimar el tiempo total (`total_minutes`) necesario para completar un pedido.

### Objetivos Específicos
1. **Preparación de Datos:**
   - Limpiar y transformar datos relacionados con órdenes, productos, shoppers y sucursales para garantizar consistencia.

2. **División de Datos:**
   - Dividir los datos en conjuntos de entrenamiento, validación y prueba para evaluar el rendimiento del modelo.

3. **Selección y Entrenamiento de Modelos:**
   - Evaluar múltiples algoritmos predictivos: Random Forest, KNN, Gradient Boosting, Linear SVC, Decision Tree, XGBoost y LightGBM.
   - Ajustar hiperparámetros para mejorar la capacidad predictiva.

4. **Predicción de `total_minutes`:**
   - Generar predicciones y completar valores nulos en el conjunto de datos de pedidos.

## Conjuntos de Datos

El proyecto utiliza los siguientes archivos CSV:

1. **`order_products.csv`:** Detalles sobre productos asociados a pedidos.
   - `order_id`: ID del pedido.
   - `product_id`: ID del producto.
   - `cantidad`: Cantidad pedida.
   - `buy_unit`: Unidad de medida (KG/UN).

2. **`orders.csv`:** Información sobre pedidos.
   - `order_id`: ID del pedido.
   - `lat`, `lng`: Coordenadas de entrega.
   - `prometido_tiempo`: Tiempo de entrega prometido.
   - `on_demand`: Indicador de entrega rápida.
   - `shopper_id`: ID del shopper asignado.
   - `store_branch_id`: ID de la sucursal.
   - `total_minutes`: Tiempo total en minutos (etiqueta).

3. **`shoppers.csv`:** Detalles sobre los compradores.
   - `shopper_id`: ID del comprador.
   - `antigüedad`: Nivel de experiencia.
   - `tasa_encontrada`: Porcentaje de productos encontrados.
   - `picking_speed`: Velocidad de picking.
   - `tasa_aceptada`: Porcentaje de pedidos aceptados.
   - `calificación`: Evaluación del cliente.

4. **`storebranch.csv`:** Detalles de las sucursales.
   - `store_branch_id`: ID de la sucursal.
   - `tienda`: Identificación de la tienda.
   - `lat`, `lng`: Coordenadas de la sucursal.

## Metodología

1. **Limpieza y Análisis de Datos:**
   - Validación de consistencia y manejo de valores nulos.

2. **Combinación de Datos:**
   - Integración de datos en un DataFrame unificado utilizando pandas.

3. **Entrenamiento de Modelos:**
   - División en conjuntos de entrenamiento, validación y prueba.
   - Pruebas con diversos modelos y selección del mejor según el RMSE.

4. **Generación de Predicciones:**
   - Aplicación del modelo seleccionado para predecir valores de `total_minutes`.

## Ejecución

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/Modelo-Predictivo-Tiempo-de-entrega-de-pedidos.git
   ```

## Resultados

- El mejor modelo fue [modelo seleccionado], con un RMSE de [valor].
- Archivo de salida: `orders.csv` con las predicciones de `total_minutes` para los pedidos.
