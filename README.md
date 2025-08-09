# Open Phone

# ToDo
- [ ] Accessories
	- [ ] Flashlight
- [ ] Human Interface
	- [ ] Vibration
	- [ ] Speaker
	- [ ] Fingerprint Sensor
- [ ] Connectivity
	- [x] Data - USB-C
		- [x] (SBUS Data)
	- [ ] (LORA communication)
		- meshtastic
	- [x] Cellular
- [ ] Sensors
	- [x] IMU
	- [x] Magnetometer
	- [ ] Fingerprint
- [ ] Video
	- [ ] Display
	- [ ] Camera
	- [ ] HDMI
- [ ] Audio
	- [ ] cellular audio $\to$ USB
	- [ ] CM5 audio IO
- [ ] Power
	- [ ] Load Switch 
		- [x] Modem
		- [ ] Camera
		- [ ] Mic
	- [x] USB-C Power delivery
	- [x] Power usage monitoring
		- [x] Current Monitor
		- [x] Voltage Monitor
# Hardware
- Back of PCB should face the screen
	- only very flat components on back
- PCB cutout for battery
    - Battery and PCB are on the same height to save space 

## Thermal management
- all significant heat producers face back
- Battery and screen keep a distance to hot spots

## Controller
Raspberry pi compute Module
https://www.raspberrypi.com/documentation/computers/compute-module.html#compute-module-5
https://datasheets.raspberrypi.com/cm5/cm5-datasheet.pdf
$\to$ 5V supply
$\to$ [Board connector](https://www.mouser.de/ProductDetail/Amphenol-FCI/10164227-1001A1RLF?qs=MyNHzdoqoQIc%2Fqhi8q%2FTOw%3D%3D)
Normalbetrieb unter Last $\to$ ~500mA

## Speicher
### SD Karte
- over SPI

## Screen
IPhone Xr 460ppi  ~6 Zoll

|                                                                                                                                                                         | size  | maße                         | resolution  | price | Flex | Händler |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- | ---------------------------- | ----------- | ----- | ---- | ------- |
| [FLEX](https://www.alibaba.com/product-detail/Super-Thin-6-67-inch-1080_1601047701892.html?spm=a2700.galleryofferlist.normal_offer.d_title.4c7013a07lG6Xn)              | 6,67" | 165,16mm x 71,532mm x 0,33mm | 1080 x 2160 | 95€   | ja   | Alibaba |
| [6" Flex](https://www.alibaba.com/product-detail/360-Degree-Bendable-6-Inch-Flexible_1600485553315.html?spm=a2700.galleryofferlist.normal_offer.d_title.4c7013a07lG6Xn) | 6"    | 68.04 x 136,08mm             | 1080 x 2160 | 95€   | ja   | Alibaba |

## Connectivity

- WLan $\to$ schon da
- Bluetooth $\to$  schon da
- micro HDMI $\to$ just add connector
- Ethernet?
- Phone network
- NFC
- USB-C
	- device mode
	- host mode
		- USB-Sticks und so
- Headphone-jack


### 3G 4G 5G

| Link                                        | Price |         |                                                                | Manual                                              |
| ------------------------------------------- | ----- | ------- | -------------------------------------------------------------- | --------------------------------------------------- |
| https://mc-technologies.com/produkt/162368/ | 70€   |         |                                                                |                                                     |
| SIM7600G-H                                  | ~40€  | mit GPS | Dev-Board müsste man nachbauen, sollte aber nicht so wild sein | https://fcc.report/FCC-ID/2AJYU-8PYA007/4857209.pdf |
|                                             |       |         |                                                                |                                                     |

[NAU8810](https://octopart.com/de/datasheet/nau8810yg-nuvoton-29622521 ) $\to$ Audio Codec
[Microphone](https://octopart.com/de/ics-40618-invensense-71346755)


## Powersupply
$\to$ 5V Akku Ladeelektronik
[load switch](https://www.ti.com/lit/ds/symlink/tps22917.pdf?ts=1749349462384)

### Battery Controller
Charge and boost controller, Power Path Management
availlable JLC
[BQ25895](https://www.ti.com/lit/ds/symlink/bq25895.pdf) ~3€


### Battery

| Kapazität                                                                                                                                               | Maße           | Preis | Händler |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ----- | ------- |
| [5000mAh](https://www.alibaba.com/product-detail/Lithium-Polymer-ultra-Thin-Lipo-3_1868172466.html?spm=a2700.details.you_may_like.3.b10c349ePAwK8i)     | 6 x 50 x 82    | 3,80€ | Alibaba |
| [5500mAh](https://www.alibaba.com/product-detail/3-7-V-407595-5500mah-Factory_62168748778.html?spm=a2700.details.you_may_like.15.6f191303vtdQ68)        | 4 x 75 x 95mm  | 6,39€ | Alibaba |
| [10000mAh](https://www.alibaba.com/product-detail/8065113-3-7V-Lipo-Battery-10000mah_62109571526.html?spm=a2700.details.you_may_like.21.6f191303vtdQ68) | 8 x 65 x 113mm | 8,50€ | Alibaba |


## Sensors

- [[Inertial Measurement Unit|IMU]]
- 3D [[Magnetometer]]
- Fingerprint sensor
	- https://biometrics.mainguet.org/types/fingerprint/product/FPC/FPC_1020_flyer.pdf
		- SPI
- Camera


