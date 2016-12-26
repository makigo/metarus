# metarus
Weather service query script is used NOAA

It works on Linux/macOS/OpenWRT

### Help

    Использование: metarus [КЛЮЧ]... [CODE]...
    
    Команды на выбор:
      -t,  --temp=code    Только темперетура.
      -d,  --decode=code  Декодированные данные.
      -c,  --city=ru      Список доступных городов в соответствии с кодами.
      -D,  --depends      Проверить все зависимости Metarus.

      -h,  --help         Показать эту справку и выйти.
      -v,  --version      Показать информацию о версии и выйти.

    Примеры:
      metarus -d uuee     Вывод декодированной информации о погоде в Москве.
      metarus -c ru       Вывод информации о кодах Российских городов.
  
### Install
Copy Metarus to /usr/local/bin  
Run "metarus --help"  
Done

### Examples
Decoded data from NOAA station (UUWW)

    Server ~ # metarus -d uuww
    Metarus pattern (UUWW) in NOAA data.
    Station       : Moscow / Vnukovo , Russia  
    Day           : Dec 26, 2016  
    Time          : 19:30 UTC 
    Wind direction: 220° (SW) 
    Wind speed    : 7.1 m/s 
    Wind gust     : --- m/s 
    Visibility    : 1.60 km 
    Temperature   : 0 °C 
    Dewpoint      : -1 °C 
    Pressure      : 751 mm Hg 
    Humidity      : 92% 
    Clouds        : mostly cloudy 
    Weather       : light snow 
  
Checking dependencies  

    Server ~ # metarus -D
    Checking depends Metarus...
    ---------------------------
       OK: curl	 found
       OK: awk	 found
       OK: cut	 found
       OK: sed	 found
  
Code - City  

    Server ~ # metarus -c ru
    RUSSIA: 
        UNAA - Abakan		    URSS - Adler		    UHMA - Anadyr
        URKA - Anapa		    ULAA - Arhangel'Sk	    URWA - Astrakhan
        UNBB - Barnaul		    UIBB - Irkutsk		    UUBP - Brjansk
        USCC - Chelyabinsk	    UIAA - Chita		    UELL - Cul'Man
        USSS - Ekaterinburg	    URWI - Elista		    UHHH - Habarovsk
        USHH - Hanty-Mansijsk	UIII - Irkutsk		    UEEE - Jakutsk
        UMKK - Kaliningrad	    UWKD - Kazan'		    UNEE - Kemerovo
        URKK - Krasnodar	    UHMM - Magadan		    URMM - Mineral'Nye Vody
        UERR - Mirny		    UUDD - Msk/Domodedovo	UUEE - Msk/Sheremet'Ye
        UUWW - Moscow/Vnukovo	ULMM - Murmansk	        URMN - Nalchik
        USNN - Nizhnevartovsk	UWGG - Nizhny Novgorod	UNWW - Novokuznetsk
        UNOO - Omsk		        UWOO - Orenburg	        UWPP - Penza
        USPP - Perm'		    UHPP - Petropavlovsk	UERP - Polyarny
        URRR - Rostov-Na-Donu	UWWW - Samara		    UWSS - Saratov
        ULLI - St. Peterburg	URMT - Stavropol	    USRR - Surgut
        UUYY - Syktyvkar	    UEST - Tiksi		    UUEM - Tver'
        UWUU - Ufa		        UIUU - Ulan-Ude	        UWLW - Ulyanovsk
        ULOL - Velikie Luki	    UHWW - Vladivostok	    URWW - Volgograd
        ULWW - Vologda		    UUOO - Voronez		    UHSS - Yuzhno-Sakhalinsk

### Contact
Email <work.makhonin@gmail.com>
