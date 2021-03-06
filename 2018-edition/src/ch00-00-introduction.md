# Вовед

> Забелешка: Ова издание на книгата е исто што и [Програмата за Rust
> Јазик] [nsprust] достапен во формат за печатење и ebook од [Не скроб]
> Прес] [nsp].

[nsprust]: https://nostarch.com/rust
[nsp]: https://nostarch.com/

Добредојдовте во * The Rust Programming Language *, воведна книга за Rust.
Програмскиот јазик "Rust" ви помага да пишувате побрз, посигурен софтвер.
Ергономијата на високо ниво и контролата на ниско ниво се честопати несогласувања во програмирањето
јазичен дизајн; Rust предизвици кои конфликт. Преку балансирање моќно
технички капацитет и одлично искуство за програмери, Rust ти дава опција
за контрола на деталите на пониско ниво (како што се користење на меморијата) без сите проблеми
традиционално поврзани со таква контрола.

## Кој е 'ржот

Rust е идеална за многу луѓе од различни причини. Ајде да погледнеме неколку од нив
најважните групи.

### Тимови на програмери

Ржа се покажа како продуктивна алатка за соработка меѓу големите тимови
програмери со различни нивоа на системско знаење за програмирање. Низок код
е склон кон различни суптилни грешки, што во повеќето други јазици може да биде
фатени само преку детално тестирање и внимателно прегледување на кодот од страна на искусни
програмери. Во Руст, компајлерот игра улога на довереник со тоа што одбива
компајлирајте го кодот со овие неостварливи грешки, вклучувајќи ги и конкурентските грешки. Со работа
заедно со компајлерот, тимот може да го помине своето време фокусирајќи се на програмата
логика, наместо да ги бркаат грешките.

Rust, исто така, носи современи алатки за развој на системот за програмирање на светот:

* Cargo, вклучениот менаџер на зависност и алатка за изградба, го прави додавањето,
  составувањето и управувањето со зависностите безболни и конзистентни низ Rust
  екосистем.
* Rustfmt обезбедува конзистентен стил на шифрирање кај програмерите.
* Серверот за Rust Language Server овластува интегрирано развојно опкружување (IDE)
  интеграција за комплетирање на кодот и пораки за грешка.

Со користење на овие и други алатки во екосистемот Руст, програмерите можат да бидат
продуктивен додека пишува системски код.

### Студентите

Rust е за учениците и за оние кои се заинтересирани да учат за системите
концепти. Користење на 'рѓа, многу луѓе научиле за теми како што работат
развој на системи. Заедницата е многу добредојдена и среќна да одговори
студентски прашања. Преку напори како што е оваа книга, тимовите на "Руст" сакаат
да направат системски концепти подостапни за повеќе луѓе, особено оние кои се нови
програмирање.

### Компании

Стотици компании, големи и мали, користат Rust во производството за различни
задачи. Овие задачи вклучуваат алатки за командната линија, веб сервиси, DevOps алатки,
вградени уреди, аудио и видео анализа и транскодиране, криптовекциите,
биоинформатиката, пребарувачите, Интернет на нештата апликации, машина
учење, па дури и главни делови на веб прелистувачот Firefox.

### развивачи на слободен софтвер

Rust е за луѓе кои сакаат да го изградат програмскиот јазик на рж, заедница,
развивачки алатки и библиотеки. Ние би сакале да имате придонес кон Rust
јазик.

### Луѓе кои ја вреднуваат брзината и стабилноста

Rust е за луѓе кои копнеат за брзина и стабилност на еден јазик. Со брзина, ние
значи брзината на програмите што можете да ги креирате со Rust и брзината на
кои Rust ви овозможува да ги напишете. Проверките на компајлерот на 'рѓата обезбедуваат стабилност
преку додавање на функции и рефакторинг. Ова е спротивно на кршливи
код за наследство на јазици без овие проверки, кои програмерите често ги имаат
се плаши да се измени. Со стремеж за апстракции со нула трошоци, функции на повисоко ниво
кои се компајлираат на пониско ниво кодот брзо како кодот напишан рачно, 'рѓа
напори да се направи безбеден код биде брз код, како и.

Јазикот "Руст" се надева дека ќе поддржува и многу други корисници; оние споменати
тука се само некои од најголемите засегнати страни. Севкупно, најголема Rust е
амбиција е да се елиминираат размени кои програмерите ги прифатија
децении со обезбедување на безбедноста * и * продуктивноста, брзината * и * ергономијата. Дај
Rust обидете се и види дали неговите избори работат за вас.

## Која е оваа книга

Оваа книга претпоставува дека сте напишале код во друг програмски јазик, но
не прави никакви претпоставки за тоа. Се обидовме да го направиме материјалот
широко достапни за оние од широк спектар на програми за потекло. Ние
не поминуваат многу време да разговараат за тоа што програмирањето * е * или како да мислите
за тоа. Ако сте сосема нови за програмирање, подобро би ни служеле
читање книга која конкретно обезбедува вовед во програмирање.

## Како да ја користите оваа книга

Општо земено, оваа книга претпоставува дека го читате во редослед од напред до
назад. Подоцна поглавја се градат врз концепти во претходните поглавја и порано
поглавја можеби нема да се истражуваат во детали за некоја тема; ние обично се враќаме на
тема во подоцнежното поглавје.

Во оваа книга ќе најдете два вида поглавја: поглавја на концептот и проект
поглавја. Во концепт поглавја, ќе дознаете за еден аспект на 'рѓа. Во проектот
поглавја, ќе градиме мали програми заедно, применувајќи го она што го научиле
далеку. Поглавјата 2, 12 и 20 се поглавја на проектот; останатите се концепт поглавја.

Поглавје 1 објаснува како да го инсталирате Руста, како да напишете Hello, world! програма,
и како да го користите Cargo, Rust's менаџер на пакети и да изгради алатка. Поглавје 2 е
практично воведување на јазикот Раг. Овде ги покриваме концептите на високо ниво
ниво, а подоцна и поглавја ќе обезбедат дополнителни детали. Ако сакате да добиете
Вашите раце веднаш валкани, Поглавје 2 е место за тоа. На прво, ти
можеби дури и сакаат да го прескокнат Поглавјето 3, кое ги покрива функциите на Раст слични на оние
на други програмски јазици, и главата веднаш до поглавје 4 за да дознаете
Систем за сопственост на Раст. Меѓутоа, ако сте особено прецизен ученик
кој претпочита да ги научи сите детали пред да се пресели во следниот, можеби ќе сакате
да го прескокнете поглавјето 2 и одете директно во Поглавје 3, враќајќи се во Поглавје 2 кога
би сакале да работите на проект со примена на деталите што сте ги научиле.

Поглавјето 5 ги разгледува структурите и методите, а поглавје 6 ги опфаќа enums, `match`
изразите и конструкцијата на "ако дозволиме". Ќе користиш структури и
enums да се направи сопствени видови во 'рѓа.

Во Поглавје 7, ќе дознаете за системот за модули на Раст и за правилата за приватност
за организирање на вашиот код и неговиот јавен интерфејс за програмирање на апликации
(API). Во Глава 8 се дискутираат некои општи структури на податоци за собирање кои
стандардна библиотека обезбедува, како што се вектори, жици и хаш мапи. Поглавје 9
ги истражува филозофијата и техниките за ракување со грешки на Раст.

Поглавје 10 копа во генерики, особини и животи, кои ви даваат моќ
за да дефинирате код кој се однесува на повеќе типови. Поглавје 11 е за тестирање,
што дури и со гаранции за сигурност на Раст е неопходно за да се обезбеди вашата програма
логиката е точна. Во Поглавје 12, ќе ја градиме сопствената имплементација на подмножество
на функционалноста од алатката за командната линија `grep` која бара текст
во рамките на датотеки. За ова, ќе користиме многу од концептите за кои дискутиравме во
претходни поглавја.

Поглавје 13 ги истражува затворачите и итераторите: карактеристики на Раста од кои доаѓаат
функционални програмски јазици. Во Поглавје 14, ќе го испитаме Карго во повеќе
длабочината и зборувајте за најдобрите практики за споделување на вашите библиотеки со други.
Во глава 15 се разгледуваат паметни покажувачи што ги нуди стандардната библиотека и
особини кои овозможуваат нивната функционалност.


Во Поглавје 16, ќе одиме низ различни модели на истовремени програми
и зборувај за тоа како Рашта ви помага да програмирате во повеќе теми бестрашно.
Во Глава 17 се разгледува како идиомите на Руст се споредуваат со објектно-ориентираното програмирање
принципи со кои можеби сте запознаени.

Поглавје 18 е референца за моделите и усогласување на моделот, кои се моќни
начини на изразување на идеи низ програмите за 'рѓа. Поглавјето 19 содржи
размена на напредни теми од интерес, вклучувајќи небезбедна Ржа и многу повеќе
за време на живот, особини, видови, функции и затворања.

Во Поглавје 20, ќе завршиме проект во кој ќе имплементираме ниско ниво
мулти-тренд веб сервер!

Конечно, некои додатоци содржат корисни информации за јазикот во
повеќе референтен формат. Додаток А ги опфаќа клучни зборови на Руст, Прилог Б
ги опфаќа операторите и симболите на Раст, Прилогот C ги опфаќа деривативните особини
обезбедени од стандардната библиотека, а Додатокот Д опфаќа макроа.

Не постои погрешен начин да се прочита оваа книга: ако сакате да прескокнете напред, одете по неа!
Можеби ќе треба да скокнете назад кон претходните поглавја ако имате искуство
конфузија. Но направете што работи за вас.

Важен дел од процесот на учење Руст е да научите како да го прочитате
пораките за грешки кои компајлерот ги прикажува: тие ќе ве водат кон работниот код.
Како таква, ние ќе обезбедиме многу примери на код кој не компајлира заедно со
пораката за грешка компајлерот ќе ви покаже во секоја ситуација. Знајте дека ако
внесувате и стартувате случаен пример, може да не компајлирате! Бидете сигурни дека ќе го прочитате
околниот текст за да се види дали треба да се користи примерот со кој се обидувате да извршите
грешка. Во повеќето ситуации, ќе ве одведеме до точната верзија на кој било код
што не се компајлира.

## Изворен код

На изворните датотеки од кои оваа книга е генерирана може да се најдат на
[GitHub] [книга].

[книга]: https://github.com/rust-lang/book/tree/master/second-edition/src
