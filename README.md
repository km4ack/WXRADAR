# WXRADAR
A Winlink Service

[Project Status](https://app.simplenote.com/publish/6zbBNy#Project_Status)

#Preface
The WXRADAR service provides amateur radio operators a way to request the latest US radar images and have them delivered to their [Winlink](https://winlink.org/) inbox. This service works with both telnet and RF for the amateur operator.

#<a id="caution"></a>Caution
When working with RF Winlink connections, we have severely limited bandwidth. Even with images as small as 10kb, typical download times are ~8-10 minutes when working with a *good* [VARA HF](https://rosmodem.wordpress.com/) connection. Under poor propagation, download times will be much longer. VARA FM is much faster and should be used when possible. Download time for VARA FM with a paid upgrade is ~60 seconds. Please use VARA FM or telnet connections to test the WXRADAR system as to avoid tying up a gateway unnecessarily.

#Usage
Using the system is as simple as sending a Winlink message to **WXRADAR** with the appropriate three character "code" in the subject line. What goes into the body of the message doesn't matter as the body is ignored. Only one code should be sent at a time. After sending your request, please allow 2-3 minutes for the system to process the request and reply. Example Winlink radar request:


	To: WXRADAR
	Subject: SMV
	Body: [anything]

#Codes
Note: Codes do not contain numbers.

| CODE       | Radar Area  |
| -----: |-----:|
| PNW |Pacific NorthWest|
| NOR  | North Rockies|
| UMS   | Upper Miss Valley |
| CGL    | Central Great Lakes |
| NOE   | Northeast |
| PSW  | Pacific Southwest |
| SOR   | Southern Rockies |
| SOP   | Southern Plains |
| SMV  | Southern Miss Valley |
| SOE   | Southeast |
| NAT   | National |
| ALA  | Alaska |
| HAW  | Hawaii |
| GUA | Guam |

#Image Compression
Care has been taken to compress the images as small as possible while retaining enough detail that the operator has good data to work with. The original images downloaded by the script are ~65kb. After compression, the resulting image sent with Winlink is ~10kb. In the Winlink image, text around the radar will be difficult to read due to the compression before the images are sent. 

#Reference

[radar.images.gov](https://radar.weather.gov/region/southmissvly/standard)

[Send images from CLI with Pat](https://groups.google.com/g/pat-users/c/s50QNa6Q4PQ/m/va4W_Vq0CQAJ)

[imagemagick resize](https://imagemagick.org/script/command-line-processing.php)

#Thanks
A special thank you to the [Stones River Amateur Radio Club](https://srarctn.org/) and Tom Delker, [K1KY](https://www.qrz.com/db/k1ky), (trustee) for allowing the use of the club call (K4FUN) for this project.

[Project Status](https://app.simplenote.com/publish/6zbBNy#Project_Status)
