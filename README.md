# project_bio

## Проект по биоинформатике 
### ВШЭ, майнор, 2 год, лето 2023

### Индивидуальная часть

Цель проекта - определить, когда в ходе эволюции появился белок, связанный с гистоновыми модификациями.

## Краткое описание гена

Белок: SETD2.

Модификация: H3K36me2.

Функция: Histone modification write. Белок SETD2 - гистоновая метилтрансфераза, специфичная для лизина 36 гистона H3. Метилирование остатка ассоциировано с активным хроматином. H3K36me предотвращает некорректную инициацию транскрипции, выполняет такие функции, как восстановление поврежденной ДНК и регуляция сплайсинга пре-мРНК. Мутации в SETD2 и в H3K36 могут приводить к развитию рака.

Ссылки на статьи: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9116022/, https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5545052/.

Комплексы: -.

Ткани: фибробласты, мозжечок, большеберцовая артерия, тестикулы, щитовидная железа, костный мозг.

Доменная структура: SET_SETD2, SRI, AWS, WW.

## Множественное белковое выравнивание для каждого из 4-х гистонов

Выравнивание белковых последовательностей было произведено в MUSCLE (https://www.ebi.ac.uk/Tools/msa/muscle/). Ниже приведены скриншоты некоторых частей выравниваний, полностью их можно посмотреть в html-файлах.

### H2A 

https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h2a.html

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h2a.png" width="350" height="400">

Аминокислотные последовательности по большей части похожи друг на друга. Они все представляют из себя белок-гистон H2A. Видимо, такие различия не влияют на функцию белка, на его свойства, поэтому существует несколько изоформ (могли появиться в ходе мутаций).

Для дальнейшего анализа была выбрана аминокислотная последовательность из файла NP_001387330.1, так как для нее есть достаточно много похожих последовательностей.

### H2B

https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h2b.html

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h2b.png" width="350" height="300">

Некоторые аминокислотные последовательности похожи друг на друга, некоторые - заметно различаются. На снимке видны как будто бы два кластера. Несмотря на это, все белковые последовательности представляют из себя белок-гистон H2B. Видимо, такие различия не влияют на функцию белка или влияют, но белок при этом все равно может выступать в качестве гистона, и поэтому есть несколько изоформ (могли появиться в ходе мутаций).

Для дальнейшего анализа была выбрана аминокислотная последовательность из файла NP_001368918.1, так как для нее есть достаточно много похожих последовательностей.

### H3

https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h3.html

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h3.png" width="350" height="200">

Гены почти полностью являются копиями друг друга.

Для дальнейшего анализа была выбрана аминокислотная последовательность из файла NP_003520.1.

### H4

https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h4.html

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/h4.png" width="350" height="200">

Гены почти полностью являются копиями друг друга.

Для дальнейшего анализа была выбрана аминокислотная последовательность из файла NP_003529.1.

## Последовательность белка 

Количество изоформ: 3.

Идентификатор белка: NP_054878.5.

Длина белка: 2564 aa. 

## Таблички с E-value и -log(E-value) для 4-х гистонов и белка

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/results.png" width="700" height="200">

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/log_results.png" width="700" height="150">

## Тепловая карта, созданная по табличке -log(E-value)

Тепловая карта отрисована с помощью библиотеки seaborn. 

<img src="https://github.com/AnyaAkhmatova/project_bio/blob/main/screenshots_and_html/heatmap.png" width="400" height="400">

## Вывод

По тепловой карте видно, что действительно при удалении от человека по эволюционной лестнице -log(E-value) уменьшается как для белка, так и для гистонов. Белок, как и гистоны, видимо, появился при возникновении одноклеточных эукориот, он (или похожие на него белки - гомологи) присутствует у позвоночных, беспозвоночных и одноклеточных эукориот, но у архей и бактерий он найден не был.

____

Все fasta и blast файлы лежат на сервере в папке auakhmatova/project/. Там же лежат таблицы в csv-файлах results.csv (копия - https://github.com/AnyaAkhmatova/project_bio/blob/main/results.csv) и log_results.csv (копия - https://github.com/AnyaAkhmatova/project_bio/blob/main/log_results.csv) и jupyter notebook ind_part.ipynb, который запускался на сервере (копия - https://github.com/AnyaAkhmatova/project_bio/blob/main/ind_part.ipynb). 
