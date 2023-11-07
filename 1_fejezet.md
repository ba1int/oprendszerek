- **2; ismertesse a megszakítások típusait, a megszakításkezelés lépéseit!**
	- Típusai:
		- Hardver megszakítás (Interrupt Request - IRQ)
			- speciális esete a nem maszkolható megszakítás
		- Kivétel
			- ezeket a processzor generálja, pl hogyha nullával való osztást kell elvégeznie, kivétel a **Trap**
		- Szoftver megszakítás
			- ezek segítségével vehetőek igénybe a rendszerhívások
	- megszakításkezelés lépései:
		- megszakításkérés -> a processzor befejezi a végzett műveletet -> a processzor elmenti a futó folyamat állapotát -> minden olyan megszakítási szint leáll, amelynek prioritása nem nagyobb az érkezett megszakításnál -> a központi egység megkeresi a kiszolgáló rutin címét és futtatja azt -> újra engedélyezi a letiltott megszakítási szinteket -> a processzor visszaállítja a folyamat állapotát, és visszaadja a vezérlést.

- **3; Ismertesse az operációs rendszerek feladatait! Milyen fő részekből áll a rendszermag?**
	- Feladatai:
		- alapfeladatuk a felhasználói folyamatok igényeinek kielégítése.
		- minden folyamat számára a szükséges erőforrások biztosítása, elosztása.
	- rendszermag(kernel) fontosabb részei:
		1. processzorkezelés
		2. memóriakezelés
		3. fájlrendszerek kezelése
		4. 

- **7; Miért előnyösek a többfeladatos rendszerek? Milyen árat kell fizetni ezekért az előnyökért?**
	- a munkafolyamatokat párhuzamosítani tudjuk
		- a számítógép egyszerre több feladatot is el tud végezni
	- ára pedig hogy több erőforrást(memória, processzor) igényel, és ha túlterheljük a rendszert, akkor lelassulhat

- **10; Ismertesse a legfontosabb Neumann-elveket! Mi a Neumann-ciklus?**
	- Neumann-elvek:
		- Tárolt program: az adatokat és az utasításokat is numerikus kódok formájában kell tárolni.
		- Kettes számrendszer(binary): adatok/programok ábrázolására kettes számrendszert kell alkalmazni (*0,1*)
		- Vezérlőegység: vezérlőegység, amely képes megkülönböztetni az utasítást az adattól, és követni az utasításokat
		- Aritmetikai-logikai egység
		- Perifériák: kapcsolat ember-gép között
		- Szekvenciális végrehajtás: utasítások egymás után
	- Neumann-ciklus:
		- memóriából lehívja, értelmezi és végrehajta az utasítást, aztán előlről kezdi, lehív, értelmez, végrehajt, lehív....
		- 

- **11; Milyen módszerekkel kommunikálhat a CPU a perifériákkal? Értékelje őket!**
	- a perifériák az operációs rendszer magját az eszközkezelőkön, és a megszakítás rendszeren keresztül tudják elérni.