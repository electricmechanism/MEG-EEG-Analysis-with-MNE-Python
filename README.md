# MEG-EEG-Analysis-with-MNE-Python
Analysis of Beta Frequency Brain Activity Using Topographic Maps In this paper, we analyzed the data of brain activity associated with right and left hand movements in the beta frequency range (β).

The aim of the study was to investigate the spatiotemporal dynamics of brain activity in the interval from -800 ms to +1600 ms relative to the stimulus/event. To visualize the results, topographic maps were constructed reflecting the distribution of activity over the surface of the head.

Methods
1. Data
The data were obtained using magnetoencephalography (MEG) or electroencephalography (EEG). The raw data contained time series for three types of conditions:

Activity during left hand movement.
Activity during right hand movement.
Difference between right and left hand activity.
The analysis was performed using averaged data across subjects (evoked_data), which increased the reliability of the results.

2. Time intervals
The analysis was performed in the time range from -800 ms to +1600 ms relative to the stimulus/event. For ease of interpretation, the data were divided into time intervals with a step of 200 ms.

For each interval, the data were averaged across all channels, which provided an idea of ​​the average brain activity at a given point in time.

3. Channel Types
Before constructing topographic maps, an analysis of the available channel types was performed:

Gradiometers (grad): Used if pairs of gradiometers could be correctly organized.
Magnetometers (mag) and EEG channels (eeg): Used as an alternative if gradiometers were missing.
If pairs of gradiometers were missing, only one channel from each pair was used. This allowed us to avoid errors when constructing graphs.

4. Constructing Topographic Maps
Topographic maps were constructed using the mne.viz.plot_topomap function, which allows us to visualize the distribution of activity over the surface of the head. For each time interval, three rows of maps were constructed:

Left hand: Displaying activity associated with the movement of the left hand.
Right hand: Displaying activity associated with the movement of the right hand.
Difference: Displaying the difference between the activity of the right and left hands.
The color scale was adjusted to reflect small changes in the data (e.g., in the range from -1e-13 to +1e-13). This allowed us to highlight significant changes in activity even at low signal amplitudes.

Results
As a result of the analysis, topographic maps were obtained that reflect the spatiotemporal dynamics of brain activity in the beta frequency. Key findings:

Spatial distribution of activity:
Left hand activity was predominantly localized in the contralateral (right) areas of the motor cortex.
Right hand activity was observed in the ipsilateral (left) areas of the motor cortex.
The difference between the activity of the right and left hands emphasized specific areas involved in the organization of movements.
Temporal dynamics:
The most pronounced activity was observed in the interval from -200 ms to +400 ms, which corresponds to the period of preparation and execution of movements.
In later intervals (> +400 ms), the activity gradually decreased, which may be associated with the completion of the motor act.
Beta frequency:
Analysis of the beta frequency revealed oscillations characteristic of the processes of inhibition and control of movements.
Discussion
The results obtained are consistent with modern concepts of the role of the motor cortex in the organization of movements. Spatial localization of activity confirms the contralateral organization of motor functions. Analysis of the beta frequency revealed key time windows in which the most significant changes in activity occur.

The use of topographic maps made it possible to clearly demonstrate the dynamics of brain activity, which makes this approach a useful tool for further research.


Анализ мозговой активности в частоте бета с использованием топографических карт
В данной работе мы провели анализ данных мозговой активности, связанных с движениями правой и левой рук, в частотном диапазоне бета (β). Целью исследования было изучение пространственно-временной динамики активности мозга в интервале от -800 мс до +1600 мс относительно стимула/события. Для визуализации результатов были построены топографические карты, отражающие распределение активности по поверхности головы. 
Методы
1. Данные
Данные были получены с использованием методов магнитоэнцефалографии (MEG) или электроэнцефалографии (EEG). Исходные данные содержали временные ряды для трех типов условий:

Активность при движении левой руки.
Активность при движении правой руки.
Разница между активностью правой и левой рук.
Для анализа были использованы усредненные данные по испытуемым (evoked_data), что позволило повысить надежность результатов.

2. Временные интервалы
Анализ проводился в диапазоне времени от -800 мс до +1600 мс относительно стимула/события. Для удобства интерпретации данные были разбиты на временные интервалы с шагом 200 мс.

Для каждого интервала данные усреднялись по всем каналам, что позволило получить представление о средней активности мозга в заданный момент времени.

3. Типы каналов
Перед построением топографических карт был проведен анализ доступных типов каналов:

Градиометры (grad): Использовались, если пары градиометров могли быть корректно организованы.
Магнитометры (mag) и ЭЭГ-каналы (eeg): Использовались как альтернатива, если градиометры отсутствовали.
Если пары градиометров отсутствовали, использовался только один канал из каждой пары. Это позволило избежать ошибок при построении графиков.

4. Построение топографических карт
Топографические карты строились с использованием функции mne.viz.plot_topomap, которая позволяет визуализировать распределение активности по поверхности головы. Для каждого временного интервала были построены три ряда карт:

Левая рука : Отображение активности, связанной с движением левой руки.
Правая рука : Отображение активности, связанной с движением правой руки.
Разница : Отображение разницы между активностью правой и левой рук.
Цветовая шкала была настроена так, чтобы отображать небольшие изменения в данных (например, в диапазоне от -1e-13 до +1e-13). Это позволило выделить значимые изменения активности даже при малых амплитудах сигналов.

Результаты
В результате анализа были получены топографические карты, отражающие пространственно-временную динамику активности мозга в частоте бета. Основные выводы:

Пространственное распределение активности :
Активность левой руки была преимущественно локализована в контралатеральных (правых) областях моторной коры.
Активность правой руки наблюдалась в ипсилатеральных (левых) областях моторной коры.
Разница между активностью правой и левой рук подчеркнула специфические зоны, участвующие в организации движений.
Временная динамика :
Наиболее выраженная активность наблюдалась в интервале от -200 мс до +400 мс, что соответствует периоду подготовки и выполнения движений.
В более поздних интервалах (> +400 мс) активность постепенно снижалась, что может быть связано с завершением двигательного акта.
Частота бета :
Анализ частоты бета позволил выявить осцилляции, характерные для процессов ингибирования и контроля движений.
Обсуждение
Полученные результаты согласуются с современными представлениями о роли моторной коры в организации движений. Пространственная локализация активности подтверждает контралатеральную организацию моторных функций. Анализ частоты бета выявил ключевые временные окна, в которых происходят наиболее значимые изменения активности.

Использование топографических карт позволило наглядно продемонстрировать динамику активности мозга, что делает данный подход полезным инструментом для дальнейших исследований.

