## Здраво свету!

Сега, кога сте го инсталирале Rust, ајде да ја напишеме вашата прва програма Rust. Тоа е
традиционални кога учат нов јазик за да напише малку програма која печати
текстот "Здраво, свет!" на екранот, па ние ќе го сториме истото тука!

> Забелешка: Оваа книга претпоставува основно познавање на командната линија. Рѓа прави
> нема конкретни барања за вашето уредување или алатки или каде што вашиот код живее, така
> ако сакате да користите интегрирана развојна околина (IDE) наместо
> командната линија, слободно користете ја омилената IDE. Многу IDE сега имаат некои
> степен на поддршка од 'рѓа; проверете ја документацијата на IDE за детали. Неодамна,
> тимот на "Rust" се фокусира на овозможување одлична IDE поддршка и напредок
> е направено брзо на тој фронт!

### Креирање на проектниот директориум

Ќе започнете со правење директориум за чување на вашиот код на 'рѓа. Не е важно
во Рашта, каде што живее вашиот код, но за вежбите и проектите во оваа книга,
ние предлагаме да се направи директориум * projects * во вашиот домашен директориум и да се чува сите
вашите проекти таму.

Отворете терминал и внесете ги следниве команди за да направите директориум * *
и директориум за Здраво, светот! проект во директориумот * projects *.

За Linux и macOS, внесете го ова:

```text
$ mkdir ~/projects
$ cd ~/projects
$ mkdir hello_world
$ cd hello_world
```

За Windows CMD, внесете го ова:

```cmd
> mkdir "%USERPROFILE%\projects"
> cd /d "%USERPROFILE%\projects"
> mkdir hello_world
> cd hello_world
```

За Windows PowerShell, внесете го ова:

```powershell
> mkdir $env:USERPROFILE\projects
> cd $env:USERPROFILE\projects
> mkdir hello_world
> cd hello_world
```

### Пишување и водење на програма за 'рѓа

Потоа направете нова изворна датотека и ја наречете * main.rs *. Датотеките за 'рѓа секогаш завршуваат со
* .rs * продолжување. Ако користите повеќе од еден збор во вашето име, користете
подвлечено да ги раздвои. На пример, користете * hello_world.rs * наместо
* helloworld.rs *.

Сега отворете ја датотеката * main.rs * што ја создадовте и внесете го кодот во листинг 1-1.

<span class = "filename"> Име на датотеката: main.rs </ span>

```rust
fn main() {
    println!("Hello, world!");
}
```

<span class = "caption"> Листата 1-1: Програма која печати "Hello, world!" </ span>

Зачувајте ја датотеката и вратете се на прозорецот на терминалот. На Linux или MacOS, внесете
следниве команди за компилација и извршување на датотеката:

```text
$ rustc main.rs
$ ./main
Hello, world!
```

На Windows, внесете ја командата `. \ Main.exe` наместо`. / Main`:

```powershell
> rustc main.rs
> .\main.exe
Hello, world!
```

Без оглед на вашиот оперативен систем, низата "Hello, world!" Треба да печати на
на терминалот. Ако не го видите овој излез, обратете се во "Решавање проблеми"
дел од делот Инсталација за начини да добиете помош.

Ако "Hello, world!" Не отпечати, честитки! Официјално напишавте 'рѓа
програма. Тоа ве прави програмер за Рѓа - добредојде!

### Анатомија на програма за 'рѓа

Ајде детално да разгледаме што се случило во вашиот Здраво, свет! програма.
Еве го првото парче од сложувалката:

```rust
fn main() {

}
```

Овие линии дефинираат функција во 'рѓа. Главната функција е посебна: тоа е
секогаш првиот код што се извршува во секоја извршна програма Rust. Првиот
line објавува функција наречена `main` која нема параметри и се враќа
ништо. Ако има параметри, тие ќе влезат во загради, `()`.

Исто така, имајте во предвид дека телото на функцијата е завиткано во визитни загради, `{}`. Рѓа
ги бара овие околу сите функционални тела. Добар стил е да го поставите отворот
кадрава заграда на истата линија како декларацијата на функцијата, додавајќи едно празно место
помеѓу.

Во времето на ова пишување, автоматска алатка за форматирање наречена `rustfmt` е
во фаза на развој. Ако сакате да се придржувате до стандардниот стил низ Рашта
проекти, `rustfmt` ќе го форматира кодот во одреден стил. Тимот на 'рѓа
планира да на крајот ја вклучи оваа алатка со стандардната дистрибуција на Раста, како
`рѓа`. Значи, во зависност од тоа кога ја читате оваа книга, веќе може да се инсталира
на вашиот компјутер! Проверете ја онлајн документацијата за повеќе детали.

Во главната функција е следниот код:

```rust
    println!("Hello, world!");
```

Оваа линија ја прави целата работа во оваа мала програма: таа го печати текстот на
екран. Постојат четири важни детали за да се забележи тука. Прво, стилот на 'рѓа е
да се вметне со четири простори, а не таб.

Второ, "println!" Повикува маглот за 'рѓа. Ако наместо тоа ја нарече функцијата, таа
ќе се внесе како `println` (без`! `). Ќе разговараме за макроата на Руст
повеќе детали во Додаток D. Засега, само треба да знаете дека користејќи `!`
значи дека повикувате макро, наместо нормална функција.

Трето, гледате `` Hello, world! '`String. Ние ја пренесуваме оваа низа како аргумент
да `println! ', а стрингот е отпечатен на екранот.

Четврто, ја завршуваме линијата со точка-запирка (`;`), што укажува на тоа
изразот е завршен, а следниот е подготвен да започне. Повеќето линии на Руст код
крајот со точка-запирка.

### Собирање и извршување се одделни чекори

Вие само го стартувате новосоздадената програма, па да го испитаме секој чекор во
процес.

Пред да ја стартувате програмата Rust, мора да ја компајлирате користејќи го компајлерот Rust со
влегувајќи во командата `rustc` и донесувајќи го името на вашата изворна датотека, како
ова:

```text
$ rustc main.rs
```

Ако имате C или C + + позадина, ќе забележите дека ова е слично на `gcc`
или `clang`. По компилирањето успешно, Rust излегува со бинарна извршна датотека.

На Linux и macOS можете да ја видите извршната датотека со внесување на командата `ls` во
вашата школка како што следува:

```text
$ ls
main  main.rs
```

Со PowerShell на Windows, можете да го користите и `ls`, но ќе видите три датотеки:

```text
> ls


    Directory: Path:\to\the\project


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----         6/1/2018   7:31 AM         137728 main.exe
-a----         6/1/2018   7:31 AM        1454080 main.pdb
-a----         6/1/2018   7:31 AM             14 main.rs
```

Со CMD на Windows, ќе го внесете следново:

```cmd
> dir /B %= the /B option says to only show the file names =%
main.exe
main.pdb
main.rs
```

Ова ја прикажува датотеката со изворниот код со * .rs * екстензија, извршна датотека
(* main.exe * на Windows, но * главна * на сите други платформи), и кога користите
CMD, датотека која содржи информации за дебагирање со * .pdb * наставката. Од
тука, ја стартувате датотеката * main * или * main.exe *, вака:

```text
$ ./main # or .\main.exe on Windows
```

Ако * main.rs * беше вашиот Здраво, светот! програма, оваа линија ќе печати `Здраво,
светот! "на вашиот терминал.

Ако сте повеќе запознаени со динамичен јазик, како што се Руби, Пајтон или
JavaScript, можеби нема да се користи за составување и водење на програма како
одделни чекори. Рѓа е * пред-време компајлиран * јазик, што значи дека можете
составете програма и му ги дадете извршната програма на некој друг, и тие можат да ја извршат
дури и без да се инсталира Rust. Ако ви даде некој * .rb *, * .py *, или
* .js * датотека, тие треба да имаат Руби, Пајтон или JavaScript имплементација
инсталирани (соодветно). Но, на тие јазици, ти треба само една команда
компајлирање и извршување на вашата програма. Сè е компромис во дизајнот на јазикот.

Само составувањето со `rustc` е во ред за едноставни програми, но како ваш проект
расте, ќе сакате да управувате со сите опции и ќе ви биде лесно да го споделите
код. Потоа, ќе ве запознаеме со алатката Cargo, која ќе ви помогне да пишувате
реални програми за Rust.