## Лабораторная работа № 1
### Разведочный анализ данных с помощью PySpark
#### Цель и задачи работы:
1. Познакомиться с понятием «большие данные» и способами их обработки;
2. Познакомиться с инструментом `Apache Spark` и возможностями, которые он предоставляет для обработки больших данных.
3. Получить навыки выполнения разведочного анализа данных использованием `pyspark`.

#### Порядок выполнения работы:
1. Установите [Docker Desktop on Windows](https://docs.docker.com/desktop/install/windows-install/).
2. Запустите `Docker Desktop` и добейтесь его работоспособности.
3. Склонируйте текущий репозиторий на компьютер:
> `$ git clone https://github.com/kpdvstu/SOBD2022.git`
4. Скачайте датасет, расположенный по адресу https://drive.google.com/file/d/1yJKqx4mhvbpwKPyJaNUq7J9cGy7wuqi5/view?usp=sharing. Распакуйте его и поместите файл `endomondoHR.json` в директорию `data` проекта (если директория отсутствует, создайте ее).
5. Откройте `Windows PowerShell` и перейдите в директорию с проектом:
> `$ cd SOBD2022`
6. Запустите докер-контейнер со средой разработки и инструментом `Apache Spark` и дождитесь завершения его работы.
> `$ docker-compose up`
7. Откройте браузер и перейдите по адресу: http://localhost:10000/lab
8. Откройте в браузере файл ноутбука с примером разведочного анализа `advanced-pyspark-for-exploratory-data-analysis.ipynb`. Изучите этот файл и запустите его.
9. **Рассмотрите датасет для дальнейшего анализа по варианту**. Список со ссылками на датасеты по вариантам приведен в *ЭИОС2 ВолгГГТУ*.

**Обратите внимание:**
* Для сокращения расчетного времени можно обрабатывать только часть датасета;
* **Плагиатные работы не принимаются!**.

10. Выполните разведочный анализ датасета с определением: 
* типов признаков в датасете; 
* пропущенных значений и их устранением; 
* выбросов и их устранением; 
* расчетом статистических показателей признаков (средних, квартилей и т.д.); 
* визуализацией распределения наиболее важных признаков; 
* корреляций между признаками.

11. Сделайте выводы по работе.
12. Напишите **главу курсовой работы** в пределах **10 страниц**, в которой опишите постановку задачи, описание датасета со ссылкой на него, проведенный разведовательный анализ и выводы.
13. Сохраните ноутбук с проведенным анализом и написанную главу курсовой в `GitHub / GitLab`.

**К отчету** следует представить репозиторий на `GitHub / GitLab` с выполненным разведочным анализом и главой курсовой работы, а также быть готовым продемонстрировать работоспособность кода и пояснить спорные моменты.

#### Список теоретических вопросов к отчету:
1. Фреймворк обработки больших данных `Apache Spark`, его назначение, функции и отличия от `Hadoop MapReduce`.
2. Понятие устойчивого распределенного набора данных (RDD). Понятие раздела RDD (partition). Способы создания RDD. Трансформации (transformations) и действия (actions). Кэширование (cache) данных в Spark.
3. RDD и PairRDD: понятие, назначение. Основные трансформации (transformations) и действия (actions) над ними.
4. Реализация концепции MapReduce в фреймворке Spark. Функции map, flatMap, mapValues, mapPartitions, reduce, reduceByKey.
5. Модели запуска Spark-приложений (YARN, Standalone, Kubernetes). Понятие драйвера (driver) и исполнителей (executors). Понятия задания (job), этапа (stage) и задачи (task). Модель ленивых вычислений (lazy) и ее применение в Spark. Понятие ориентированного ациклического графа (Directed Acyclic Graph, DAG).
6. Операция перемешивания данных (shuffle): причины возникновения, влияние на производительность. Класс Partitioner. Пути повышения производительности.
7. Понятие датафрейма в Spark. Основные операции над датафреймами. Скалярные функции, агрегирующие функции, оконные функции. Оптимизация запросов. Catalyst.
8. Клиентский (client) и кластерный (cluster) режимы работы Apache Spark.

#### Литература для подготовки к отчету:
1. Изучаем Spark: молниеносный анализ данных / Х. Карау, Э. Конвински, П. Венделл, М.М. Захария // ДМК Пресс, 2015. — 304 с.: ил.
2. Data Exploration // Learning Apache Spark with Python [Электронный  ресурс] / W. Feng. - [2021]. - Режим доступа : https://runawayhorse001.github.io/LearningApacheSpark/exploration.html (дата обращ. 19.09.2022).
3. Advanced Pyspark for Exploratory Data Analysis [Электронный  ресурс]. – [2022]. – Режим доступа : https://www.kaggle.com/code/tientd95/advanced-pyspark-for-exploratory-data-analysis (дата обращ. 19.09.2022). 
4. Exploratory Data Analysis (EDA) with PySpark on Databricks [Электронный  ресурс]. – [2020]. – Режим доступа : https://towardsdatascience.com/exploratory-data-analysis-eda-with-pyspark-on-databricks-e8d6529626b1 (дата обращ. 19.09.2022).
5. Exploratory data analysis with pySpark [Электронный  ресурс]. – [2020]. – Режим доступа : https://github.com/roshankoirala/pySpark_tutorial/blob/master/Exploratory_data_analysis_with_pySpark.ipynb (дата обращ. 19.09.2022).
6. Официальный сайт Apache Spark [Электронный  ресурс]. – [2022]. – Режим доступа : https://spark.apache.org/ (дата обращ. 19.09.2022).
7. Уайт, Т. Hadoop: Подробное руководство / Т. Уайт. — 3-е изд. — СПб. : Питер, 2013. — 672 с.: ил.
