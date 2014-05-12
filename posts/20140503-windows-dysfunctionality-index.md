title: Windows Dysfunctionality Index
created: 2014/05/03 16:52:22
tags: tech stuff, windows

Помимо [WEI](http://en.wikipedia.org/wiki/Windows_System_Assessment_Tool), в Windows должен быть ещё один важный показатель — коэффициент кривизны функционирования Всего, или Windows Dysfunctionality Index. После установки он равен нулю, но по мере того как в системе что-то меняется, или просто время течёт своим чередом, величина растёт.

Когда величина достигает, скажем, 5 баллов, пользователю пора звать слесаря по компьютерам, который сможет снизить это значение. А если пользователь сэкономит и дотерпит до 10 — пиши пропало, пора всё переустанавливать.

---

В свете последнего «переполнения» ОС на рабочем десктопе, захотелось предотвратить трату времени на этом перодически необходимом, рутинном и плохо автоматизируемом процессе. Нужен какой-то максимально гигиеничный способ содержания Windows на рабочей машине. И более предсказуемый и неубиваемый, чем встроенный бекап.

Пока виден такой вариант: поставить bare-metal гипервизор типа VMware ESX, создать единственную виртуальную машину, для которой выделить все доступные ресурсы, и добавить в систему отдельный жёсткий диск для снапшотов.

Сразу после активации Windows и установки всего нужного софта, сделать снапшот, и дальше просто работать в этой виртуальной машине. Если ОС замусорится — не тратить время на прочистку канализации, а восстановить сразу всё.

Это должно быть относительно быстрой процедурой, требующей минимального вмешательства. Все данные, естесственно, нужно держать либо в облаках, либо на внешних по отношению к виртуальной машине драйвах.