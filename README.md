# **Scientific Machine Learning (SciML)**

Bienvenidos a los apuntes de **Scientific Machine Learning**.
🤓

Estos notebooks recorren los fundamentos matemáticos, los métodos numéricos y su conexión con el aprendizaje de modelos científicos. Los capítulos desarrollados incluyen explicaciones en español, fórmulas, ejemplos en Python y gráficos. Los ejemplos nuevos generan sus propios datos y se pueden ejecutar en CPU.

## Cómo estudiar y ejecutar los notebooks

Sigue el temario en orden si estás comenzando. En cada notebook lee la teoría, ejecuta las celdas de arriba hacia abajo y compara los resultados con la interpretación que acompaña a los gráficos. Antes de cambiar parámetros, ejecuta el ejemplo original; después prueba los ejercicios y revisa cómo cambian el error y la estabilidad.

Desde esta carpeta, crea un entorno con Python 3.10 o posterior e instala las librerías:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install "torch>=2.14.1,<3" --index-url https://download.pytorch.org/whl/cpu
python -m pip install -r requirements.txt
python -m ipykernel install --prefix .venv --name scientific-ml --display-name "Python (Scientific ML)"
```

En Windows, activa el entorno con `.venv\Scripts\activate` y usa `python` en lugar de `python3`. En VS Code selecciona **Python (Scientific ML)** como kernel. También puedes abrir el material con `jupyter lab` desde el entorno activado. Los notebooks previos pueden conservar el nombre de un kernel del autor; selecciona el entorno que acabas de crear para ejecutarlos.

NumPy y SciPy se usan para cálculo numérico, SymPy para cálculo simbólico, Matplotlib para gráficos, pandas para tablas, scikit-learn para modelos estadísticos y PyTorch para redes y diferenciación automática. Los ejercicios de GPU detectan si CUDA está disponible y ofrecen ejecución en CPU; instalar estas dependencias no garantiza disponibilidad de CUDA.

La instalación anterior utiliza PyTorch para CPU. Si quieres ejecutar los ejercicios con una GPU NVIDIA, elige la instalación correspondiente a tu sistema en la [guía oficial de PyTorch](https://pytorch.org/get-started/locally/) antes de instalar el resto de las dependencias.

El entorno utilizado para comprobar los ejemplos nuevos fue Python 3.10.12, NumPy 2.2.6, SciPy 1.15.3, Matplotlib 3.10.9, SymPy 1.14.0, scikit-learn 1.7.2 y PyTorch 2.14.1 en CPU. [requirements.txt](./requirements.txt) permite instalar versiones compatibles; los resultados exactos y los tiempos pueden variar entre versiones y equipos. Los gráficos están guardados en los propios notebooks.

Una ruta para conectar los conceptos con SciML es: **ODE (5) → errores y solvers (6–9) → optimización (10) → ML y redes (11–12) → modelos e inversión (13–14) → PINNs, operadores y modelos diferenciables (15)**. Los capítulos 16–21 amplían incertidumbre, asimilación, computación, software, investigación y matemáticas avanzadas.

## **Temario**

| **1. CÁLCULO**                                                       |
| -------------------------------------------------------------------- |
| [1.1 Precálculo](./1_CALCULO/1_1_Precalculo.ipynb)                   |
| [1.2 Cálculo diferencial](./1_CALCULO/1_2_Calculo_diferencial.ipynb) |
| [1.3 Cálculo integral](./1_CALCULO/1_3_Calculo_integral.ipynb)       |
| [1.4 Series](./1_CALCULO/1_4_Series.ipynb)                           |

---

[🔼](#temario)

---

| **2.ÁLGEBRA LINEAL**                                                                      |
| ----------------------------------------------------------------------------------------- |
| [2.1 Vectores](./2_ALGEBRA_LINEAL/2_1_Vectores.ipynb)                                     |
| [2.2 Matrices](./2_ALGEBRA_LINEAL/2_2_Matrices.ipynb)                                     |
| [2.3 Espacios vectoriales](./2_ALGEBRA_LINEAL/2_3_Espacios_vectoriales.ipynb)             |
| [2.4 Autovalores y autovectores](./2_ALGEBRA_LINEAL/2_4_Autovalores_y_autovectores.ipynb) |
| [2.5 SVD](./2_ALGEBRA_LINEAL/2_5_SVD.ipynb)                                               |
| [2.6 Álgebra lineal numérica](./2_ALGEBRA_LINEAL/2_6_Algebra_lineal_numerica.ipynb)       |

---

[🔼](#temario)

---

| **3.PROBABILIDAD Y ESTADÍSTICA**                                                          |
| ----------------------------------------------------------------------------------------- |
| [3.1 Probabilidad](./3_PROBABILIDAD_Y_ESTADISTICA/3_1_Probabilidad.ipynb)                 |
| [3.2 Distribuciones](./3_PROBABILIDAD_Y_ESTADISTICA/3_2_Distribuciones.ipynb)             |
| [3.3 Estadística](./3_PROBABILIDAD_Y_ESTADISTICA/3_3_Estadistica.ipynb)                   |
| [3.4 Probabilidad para ML](./3_PROBABILIDAD_Y_ESTADISTICA/3_4_Probabilidad_para_ML.ipynb) |

---

[🔼](#temario)

---

| **4.CÁLCULO MULTIVARIABLE**                                                                  |
| -------------------------------------------------------------------------------------------- |
| [4.1 Funciones multivariables](./4_CALCULO_MULTIVARIABLE/4_1_Funciones_multivariables.ipynb) |
| [4.2 Derivadas parciales](./4_CALCULO_MULTIVARIABLE/4_2_Derivadas_parciales.ipynb)           |
| [4.3 Jacobiano](./4_CALCULO_MULTIVARIABLE/4_3_Jacobiano.ipynb)                               |
| [4.4 Hessiano](./4_CALCULO_MULTIVARIABLE/4_4_Hessiano.ipynb)                                 |
| [4.5 Integrales múltiples](./4_CALCULO_MULTIVARIABLE/4_5_Integrales_multiples.ipynb)         |
| [4.6 Cálculo vectorial](./4_CALCULO_MULTIVARIABLE/4_6_Calculo_vectorial.ipynb)               |

---

[🔼](#temario)

---

| **5.ECUACIONES DIFERENCIALES**                                                       |
| ----------------------------------------------------------------------------------- |
| [5.1 ODE](./5_ECUACIONES_DIFERENCIALES/5_1_ODE.ipynb)                               |
| [5.2 Sistemas dinámicos](./5_ECUACIONES_DIFERENCIALES/5_2_Sistemas_dinamicos.ipynb) |
| [5.3 Sistemas lineales](./5_ECUACIONES_DIFERENCIALES/5_3_Sistemas_lineales.ipynb)   |
| [5.4 Fourier](./5_ECUACIONES_DIFERENCIALES/5_4_Fourier.ipynb)                       |

---

[🔼](#temario)

---

| **6.ANÁLISIS NUMÉRICO**                                                                |
| -------------------------------------------------------------------------------------- |
| [6.1 Errores](./6_ANALISIS_NUMERICO/6_1_Errores.ipynb)                                 |
| [6.2 Root finding](./6_ANALISIS_NUMERICO/6_2_Root_finding.ipynb)                       |
| [6.3 Interpolación](./6_ANALISIS_NUMERICO/6_3_Interpolacion.ipynb)                     |
| [6.4 Integración numérica](./6_ANALISIS_NUMERICO/6_4_Integracion_numerica.ipynb)       |
| [6.5 Diferenciación numérica](./6_ANALISIS_NUMERICO/6_5_Diferenciacion_numerica.ipynb) |

---

[🔼](#temario)

---

| **7.MÉTODOS NUMÉRICOS PARA ODE**                                                        |
| --------------------------------------------------------------------------------------- |
| [7.1 Euler](./7_METODOS_NUMERICOS_PARA_ODE/7_1_Euler.ipynb)                             |
| [7.2 Heun](./7_METODOS_NUMERICOS_PARA_ODE/7_2_Heun.ipynb)                               |
| [7.3 Midpoint](./7_METODOS_NUMERICOS_PARA_ODE/7_3_Midpoint.ipynb)                       |
| [7.4 Runge-Kutta](./7_METODOS_NUMERICOS_PARA_ODE/7_4_Runge_Kutta.ipynb)                 |
| [7.5 Métodos adaptativos](./7_METODOS_NUMERICOS_PARA_ODE/7_5_Metodos_adaptativos.ipynb) |
| [7.6 Métodos implícitos](./7_METODOS_NUMERICOS_PARA_ODE/7_6_Metodos_implicitos.ipynb)   |
| [7.7 Stability](./7_METODOS_NUMERICOS_PARA_ODE/7_7_Stability.ipynb)                     |

---

[🔼](#temario)

---

| **8.PDE**                                                    |
| ------------------------------------------------------------ |
| [8.1 PDE fundamentales](./8_PDE/8_1_PDE_fundamentales.ipynb) |

---

[🔼](#temario)

---

| **9.MÉTODOS NUMÉRICOS PARA PDE**                                                                  |
| ------------------------------------------------------------------------------------------------- |
| [9.1 Finite Difference Method](./9_METODOS_NUMERICOS_PARA_PDE/9_1_Finite_Difference_Method.ipynb) |
| [9.2 Finite Element Method](./9_METODOS_NUMERICOS_PARA_PDE/9_2_Finite_Element_Method.ipynb)       |
| [9.3 Finite Volume Method](./9_METODOS_NUMERICOS_PARA_PDE/9_3_Finite_Volume_Method.ipynb)         |
| [9.4 Spectral Methods](./9_METODOS_NUMERICOS_PARA_PDE/9_4_Spectral_Methods.ipynb)                 |

---

[🔼](#temario)

---

| **10.OPTIMIZACIÓN**                                                                    |
| -------------------------------------------------------------------------------------- |
| [10.1 Optimización matemática](./10_OPTIMIZACION/10_1_Optimizacion_matematica.ipynb)   |
| [10.2 Gradient methods](./10_OPTIMIZACION/10_2_Gradient_methods.ipynb)                 |
| [10.3 Segundo orden](./10_OPTIMIZACION/10_3_Segundo_orden.ipynb)                       |
| [10.4 Optimización restringida](./10_OPTIMIZACION/10_4_Optimizacion_restringida.ipynb) |

---

[🔼](#temario)

---

| **11.MACHINE LEARNING**                                                                          |
| ------------------------------------------------------------------------------------------------ |
| [11.1 Supervised Learning](./11_MACHINE_LEARNING/11_1_Supervised_Learning.ipynb)                 |
| [11.2 Modelos](./11_MACHINE_LEARNING/11_2_Modelos.ipynb)                                         |
| [11.3 Unsupervised Learning](./11_MACHINE_LEARNING/11_3_Unsupervised_Learning.ipynb)             |
| [11.4 Statistical Learning Theory](./11_MACHINE_LEARNING/11_4_Statistical_Learning_Theory.ipynb) |

---

[🔼](#temario)

---

| **12.DEEP LEARNING**                                                                    |
| --------------------------------------------------------------------------------------- |
| [12.1 Neural Networks](./12_DEEP_LEARNING/12_1_Neural_Networks.ipynb)                   |
| [12.2 Arquitecturas](./12_DEEP_LEARNING/12_2_Arquitecturas.ipynb)                       |
| [12.3 Deep Learning matemático](./12_DEEP_LEARNING/12_3_Deep_Learning_matematico.ipynb) |

---

[🔼](#temario)

---

| **13.MODELAMIENTO CIENTÍFICO**                                                  |
| ------------------------------------------------------------------------------- |
| [13.1 Modelos físicos](./13_MODELAMIENTO_CIENTIFICO/13_1_Modelos_fisicos.ipynb) |

---

[🔼](#temario)

---

| **14.PROBLEMAS INVERSOS**                                                      |
| ------------------------------------------------------------------------------ |
| [14.1 PROBLEMAS INVERSOS](./14_PROBLEMAS_INVERSOS/14_1_Problema_inverso.ipynb) |

---

[🔼](#temario)

---

| **15.SCIENTIFIC MACHINE LEARNING**                                                                                    |
| --------------------------------------------------------------------------------------------------------------------- |
| [15.1 Physics-Informed Neural Networks](./15_SCIENTIFIC_MACHINE_LEARNING/15_1_Physics_Informed_Neural_Networks.ipynb) |
| [15.2 PINNs — sílabus completo](./15_SCIENTIFIC_MACHINE_LEARNING/15_2_PINNs.ipynb)                                    |
| [15.3 Neural Operators](./15_SCIENTIFIC_MACHINE_LEARNING/15_3_Neural_Operators.ipynb)                                 |
| [15.4 Reduced Order Modeling](./15_SCIENTIFIC_MACHINE_LEARNING/15_4_Reduced_Order_Modeling.ipynb)                     |
| [15.5 Neural ODEs](./15_SCIENTIFIC_MACHINE_LEARNING/15_5_Neural_ODEs.ipynb)                                           |
| [15.6 Differentiable Physics](./15_SCIENTIFIC_MACHINE_LEARNING/15_6_Differentiable_Physics.ipynb)                     |

---

[🔼](#temario)

---

| **16.UNCERTAINTY QUANTIFICATION**                                                                        |
| -------------------------------------------------------------------------------------------------------- |
| [16.1 UNCERTAINTY QUANTIFICATION](./16_UNCERTAINTY_QUANTIFICATION/16_1_UNCERTAINTY_QUANTIFICATION.ipynb) |

---

[🔼](#temario)

---

| **17.DATA ASSIMILATION**                                                      |
| ----------------------------------------------------------------------------- |
| [17.1 DATA ASSIMILATION](./17_DATA_ASSIMILATION/17_1_DATA_ASSIMILATION.ipynb) |

---

[🔼](#temario)

---

| **18.HPC COMPUTACIÓN CIENTÍFICA**                                                            |
| -------------------------------------------------------------------------------------------- |
| [18.1 Performance](./18_HPC_COMPUTACION_CIENTIFICA/18_1_Performance.ipynb)                   |
| [18.2 GPU](./18_HPC_COMPUTACION_CIENTIFICA/18_2_GPU.ipynb)                                   |
| [18.3 Parallel computing](./18_HPC_COMPUTACION_CIENTIFICA/18_3_Parallel_computing.ipynb)     |
| [18.4 Scientific computing](./18_HPC_COMPUTACION_CIENTIFICA/18_4_Scientific_computing.ipynb) |

---

[🔼](#temario)

---

| **19.SOFTWARE CIENTÍFICO**                                                          |
| ----------------------------------------------------------------------------------- |
| [19.1 SOFTWARE CIENTÍFICO](./19_SOFTWARE_CIENTIFICO/19_1_SOFTWARE_CIENTIFICO.ipynb) |

---

[🔼](#temario)

---

| **20.INVESTIGACIÓN**                                                          |
| ----------------------------------------------------------------------------- |
| [20.1 Leer papers](./20_INVESTIGACION/20_1_papers.ipynb)                      |
| [20.2 Reproducir papers](./20_INVESTIGACION/20_2_Reproducir_papers.ipynb)     |
| [20.3 Diseño experimental](./20_INVESTIGACION/20_3_Diseño_experimental.ipynb) |

---

[🔼](#temario)

---

| **21.MATEMÁTICA MÁS AVANZADA**                                                        |
| ------------------------------------------------------------------------------------- |
| [21.1 Análisis real](./21_MATEMATICA_MAS_AVANZADA/21_1_Analisis_real.ipynb)           |
| [21.2 Análisis funcional](./21_MATEMATICA_MAS_AVANZADA/21_2_Analisis_funcional.ipynb) |
| [21.3 PDE avanzada](./21_MATEMATICA_MAS_AVANZADA/21_3_PDE_avanzada.ipynb)             |

---

[🔼](#temario)

---
# SCIENTIFIC_MACHINE_LEARNING
