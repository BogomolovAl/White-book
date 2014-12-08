Перенесёмся в 20xx год, когда награда за блок умерла, и жиреют майнеры только за счёт комиссий.

Жиреют ли? Вычислим количество добываемых майнером биткойнов в секунду:

![1](http://latex.codecogs.com/gif.latex?%5Ctext%7Bincome%20(in%20USD)%7D%20%3D%20%5Cfrac%7B%5Ctext%7Bfee%20from%20block%20in%20USD%7D%7D%7B%5Ctext%7Baverage%20time%20of%20finding%20a%20block%7D%7D)

где fee from block in USD чему-то там равно, а именно,

![2](http://latex.codecogs.com/gif.latex?%5Ctext%7Bfee%20from%20block%20in%20USD%7D%20%3D%20%5Ctext%7Baverage%20transaction%20fee%20in%20USD%7D%20%5Ccdot%20%28%5Ctext%7BTPS%7D%20%5Ccdot%20600%29)

average time of finding a block тоже чему-то равно:

![3](http://latex.codecogs.com/gif.latex?%5Ctext%7Baverage%20time%20of%20finding%20a%20block%7D%20%3D%20%5Cfrac%7B2%5E%7B32%7D%20%5Ccdot%20%5Ctext%7Bdiff%7D%7D%7B%5Ctext%7Bhashrate%7D%7D)

так что окончательно имеем

![4](http://latex.codecogs.com/gif.latex?%5Ctext%7Bincome%20%28in%20USD%29%7D%20%3D%20%5Cfrac%7B%5Ctext%7Baverage%20transaction%20fee%20in%20USD%7D%20%5Ccdot%20%28%5Ctext%7BTPS%7D%20%5Ccdot%20600%29%20%5Ccdot%20%5Ctext%7Bhashrate%7D%7D%7B2%5E%7B32%7D%20%5Ccdot%20%5Ctext%7Bdiff%7D%7D)

Опустив в этом вычислении цену покупки АСИКа (сделав вид, что АСИК достался нам бесплатно), посчитаем секундный расход майнера:

![5](http://latex.codecogs.com/gif.latex?%5Ctext%7Bcost%20%28in%20USD%29%7D%20%3D%200.12%20%5Chskip%203%20pt%20%5Cfrac%7B%5C%24%7D%7B%5Ctext%7B%281000%20W%29%7D%20%5Ccdot%20%5Ctext%7B%283600%20sec%29%7D%7D%20%5Ccdot%20%5Ctext%7BW%7D%20%3D%20%5Cfrac%7B0.12%7D%7B3600000%7D%20%5Chskip%203%20pt%20%5Cfrac%7B%5C%24%7D%7B%5Ctext%7BkW%7D%20%5Ccdot%20%5Ctext%7Bhour%7D%7D%20%5Ccdot%20%5Ctext%7BW%7D)

или, убрав размерности,

![6](http://latex.codecogs.com/gif.latex?%5Ctext%7Bcost%20%28in%20USD%29%7D%20%3D%20%5Cfrac%7B0.12%7D%7B3600000%7D%20%5Ccdot%20%5Ctext%7BW%7D)

(Взята цена на электричество в 0.12$ за киловатт-час.)

Мы вычислили доход майнера за 1 секунду и его расходы на электричество за это же время. Условие, при котором держать АСИКи включенными выгодно, получается,

![7](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Ctext%7Baverage%20transaction%20fee%20in%20USD%7D%20%5Ccdot%20%28%5Ctext%7BTPS%7D%20%5Ccdot%20600%29%20%5Ccdot%20%5Ctext%7Bhashrate%7D%7D%7B2%5E%7B32%7D%20%5Ccdot%20%5Ctext%7Bdiff%7D%7D%20%3E%20%5Cfrac%7B0.12%7D%7B3600000%7D%20%5Ccdot%20%5Ctext%7BW%7D)

#### Мне неинтересно, при каком условии держать АСИКи включенными выгодно, мне интересно, покупать ли мне АСИК.

![8](http://s5.pikabu.ru/images/big_size_comm/2014-07_3/14051731795923.jpg)

Значит, прибыль (или убыток:) ) в долларах за 1 секунду, получается, равна

![9](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Ctext%7Baverage%20transaction%20fee%20in%20USD%7D%20%5Ccdot%20%28%5Ctext%7BTPS%7D%20%5Ccdot%20600%29%20%5Ccdot%20%5Ctext%7Bhashrate%7D%7D%7B2%5E%7B32%7D%20%5Ccdot%20%5Ctext%7Bdiff%7D%7D%20-%20%5Cfrac%7B0.12%7D%7B3600000%7D%20%5Ccdot%20%5Ctext%7BW%7D)

Значит, прибыль в долларах за время dt равна

![10](http://latex.codecogs.com/gif.latex?du%20%3D%20%5CBig%28%5Cfrac%7B%5Ctext%7Baverage%20transaction%20fee%20in%20USD%7D%20%5Ccdot%20%28%5Ctext%7BTPS%7D%20%5Ccdot%20600%29%20%5Ccdot%20%5Ctext%7Bhashrate%7D%7D%7B2%5E%7B32%7D%20%5Ccdot%20%5Ctext%7Bdiff%7D%7D%20-%20%5Cfrac%7B0.12%5Ccdot%5Ctext%7BW%7D%7D%7B3600000%7D%20%5CBig%29%20%5Ccdot%20%5Cfrac%7Bdt%7D%7B%5Ctext%7B1%20sec%7D%7D)

Предположив, что АСИК последней модели всегда будет стоить 3000$, окончательно получим условие выгодности покупки АСИКа:

![100](http://latex.codecogs.com/gif.latex?%5Cint%5Climits_%7B%5CSigma%7D%20%5CBig%28%5Cfrac%7B%5Ctext%7Baverage%20transaction%20fee%20in%20USD%7D%20%5Ccdot%20%28%5Ctext%7BTPS%7D%20%5Ccdot%20600%29%20%5Ccdot%20%5Ctext%7Bhashrate%7D%7D%7B2%5E%7B32%7D%20%5Ccdot%20%5Ctext%7Bdiff%7D%7D%20-%20%5Cfrac%7B0.12%5Ccdot%5Ctext%7BW%7D%7D%7B3600000%7D%20%5CBig%29%20%5Ccdot%20%5Cfrac%7Bdt%7D%7B%5Ctext%7B1%20sec%7D%7D%20%3E%203000)

где интеграл берёмся по всем временам начиная с момента покупки таким, что подынтегральное выражение больше нуля (мы предполагаем, что майнер не долбоёб и отключает свой АСИК, когда майнинг становится майнингом "в минус").