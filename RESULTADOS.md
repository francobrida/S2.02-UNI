# 📊 Análisis de Consultas SQL


## 📈 Resumen
✅ 19 correctas de 26 queries

## ✅ Query 1: Correcto

⏱ Tiempo: 0.39 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 2: Correcto

⏱ Tiempo: 0.34 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 3: Correcto

⏱ Tiempo: 0.32 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 4: Correcto

⏱ Tiempo: 0.31 ms
🔍 No se usó ningún índice en esta consulta.

---

## ❌ Query 5: Incorrecto
```diff
--- 
+++ 
@@ -1,7 +1,7 @@
-id | nombre | cuatrimestre | curso | id_grado
-72.00 | Bases moleculares del desarrollo vegetal | 1.00 | 3.00 | 7.00
-73.00 | Fisiología animal | 1.00 | 3.00 | 7.00
-74.00 | Metabolismo y biosíntesis de biomoléculas | 1.00 | 3.00 | 7.00
-75.00 | Operaciones de separación | 1.00 | 3.00 | 7.00
-76.00 | Patología molecular de plantas | 1.00 | 3.00 | 7.00
-77.00 | Técnicas instrumentales básicas | 1.00 | 3.00 | 7.00
+id | nombre | cuatrimestre | id_grado
+72.00 | Bases moleculares del desarrollo vegetal | 1.00 | 7.00
+73.00 | Fisiología animal | 1.00 | 7.00
+74.00 | Metabolismo y biosíntesis de biomoléculas | 1.00 | 7.00
+75.00 | Operaciones de separación | 1.00 | 7.00
+76.00 | Patología molecular de plantas | 1.00 | 7.00
+77.00 | Técnicas instrumentales básicas | 1.00 | 7.00
```

⏱ Tiempo: 0.33 ms
✅ Se usó índice(s) en la consulta: id_grado

---

## ✅ Query 6: Correcto

⏱ Tiempo: 0.41 ms
✅ Se usó índice(s) en la consulta: PRIMARY, PRIMARY,id_departamento

---

## ✅ Query 7: Correcto

⏱ Tiempo: 0.58 ms
✅ Se usó índice(s) en la consulta: PRIMARY,id_asignatura,id_curso_escolar, PRIMARY, PRIMARY,nif

---

## ✅ Query 8: Correcto

⏱ Tiempo: 0.38 ms
✅ Se usó índice(s) en la consulta: PRIMARY, PRIMARY,id_departamento, id_profesor,id_grado

---

## ✅ Query 9: Correcto

⏱ Tiempo: 0.38 ms
✅ Se usó índice(s) en la consulta: PRIMARY,id_curso_escolar, PRIMARY

---

## ❌ Query 10: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-departamento | apellido1 | apellido2 | nombre
+nombre | apellido1 | apellido2 | nombre
 Agronomía | Monahan | Murray | Micaela
 Economía y Empresa | Fahey | Considine | Antonio
 Economía y Empresa | Lemke | Rutherford | Cristina
```

⏱ Tiempo: 0.41 ms
✅ Se usó índice(s) en la consulta: PRIMARY

---

## ✅ Query 11: Correcto

⏱ Tiempo: 0.31 ms
🔍 No se usó ningún índice en esta consulta.

🚨 **Problemas detectados:**
🚨 `JOIN` sin índice. Revisar claves foráneas e índices.

---

## ✅ Query 12: Correcto

⏱ Tiempo: 0.32 ms
✅ Se usó índice(s) en la consulta: id_departamento

---

## ✅ Query 13: Correcto

⏱ Tiempo: 0.37 ms
✅ Se usó índice(s) en la consulta: PRIMARY, id_profesor

---

## ✅ Query 14: Correcto

⏱ Tiempo: 0.31 ms
✅ Se usó índice(s) en la consulta: id_profesor

---

## ❌ Query 15: Incorrecto
```diff
--- 
+++ 
@@ -1,5 +1,4 @@
 nombre
-Informática
 Matemáticas
 Economía y Empresa
 Educación
```

⏱ Tiempo: 0.37 ms
✅ Se usó índice(s) en la consulta: id_departamento, id_profesor

---

## ✅ Query 16: Correcto

⏱ Tiempo: 0.33 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 17: Correcto

⏱ Tiempo: 0.34 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 18: Correcto

⏱ Tiempo: 0.38 ms
✅ Se usó índice(s) en la consulta: PRIMARY, id_departamento

---

## ✅ Query 19: Correcto

⏱ Tiempo: 0.36 ms
✅ Se usó índice(s) en la consulta: id_departamento

---

## ❌ Query 20: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-grau | total
+grado | total
 Grado en Ingeniería Informática (Plan 2015) | 51.00
 Grado en Biotecnología (Plan 2015) | 32.00
 Grado en Ingeniería Agrícola (Plan 2015) | 0.00
```

⏱ Tiempo: 0.33 ms
✅ Se usó índice(s) en la consulta: id_grado

---

## ❌ Query 21: Incorrecto
```diff
--- 
+++ 
@@ -1,2 +1,2 @@
-grau | total
+grado | total
 Grado en Ingeniería Informática (Plan 2015) | 51.00
```

⏱ Tiempo: 0.36 ms
✅ Se usó índice(s) en la consulta: id_grado, PRIMARY

---

## ❌ Query 22: Incorrecto
```diff
--- 
+++ 
@@ -1,6 +1,14 @@
-grau | tipo | total_creditos
+grado | tipo | total_creditos
+Grado en Ingeniería Agrícola (Plan 2015) | NULL | NULL
+Grado en Ingeniería Eléctrica (Plan 2014) | NULL | NULL
+Grado en Ingeniería Electrónica Industrial (Plan 2010) | NULL | NULL
+Grado en Ingeniería Informática (Plan 2015) | optativa | 180.00
+Grado en Ingeniería Informática (Plan 2015) | obligatoria | 54.00
 Grado en Ingeniería Informática (Plan 2015) | básica | 72.00
-Grado en Ingeniería Informática (Plan 2015) | obligatoria | 54.00
-Grado en Ingeniería Informática (Plan 2015) | optativa | 180.00
+Grado en Ingeniería Mecánica (Plan 2010) | NULL | NULL
+Grado en Ingeniería Química Industrial (Plan 2010) | NULL | NULL
+Grado en Biotecnología (Plan 2015) | obligatoria | 120.00
 Grado en Biotecnología (Plan 2015) | básica | 60.00
-Grado en Biotecnología (Plan 2015) | obligatoria | 120.00
+Grado en Ciencias Ambientales (Plan 2009) | NULL | NULL
+Grado en Matemáticas (Plan 2010) | NULL | NULL
+Grado en Química (Plan 2009) | NULL | NULL
```

⏱ Tiempo: 0.36 ms
✅ Se usó índice(s) en la consulta: id_grado

---

## ✅ Query 23: Correcto

⏱ Tiempo: 0.36 ms
✅ Se usó índice(s) en la consulta: PRIMARY, id_curso_escolar

---

## ✅ Query 24: Correcto

⏱ Tiempo: 0.39 ms
✅ Se usó índice(s) en la consulta: PRIMARY, PRIMARY,nif, id_profesor

---

## ❌ Query 25: Incorrecto
```diff
--- 
+++ 
@@ -1,2 +1,2 @@
-id | nif | nombre | apellido1 | apellido2 | ciudad | direccion | telefono | fecha_nacimiento | sexo | tipo
-4.00 | 17105885A | Pedro | Heller | Pagac | Almería | C/ Estrella fugaz | NULL | 2000-10-05 | H | alumno
+nombre | apellido1 | apellido2 | fecha_nacimiento
+Pedro | Heller | Pagac | 2000-10-05
```

⏱ Tiempo: 0.33 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 26: Correcto

⏱ Tiempo: 0.36 ms
✅ Se usó índice(s) en la consulta: PRIMARY, id_profesor

---
