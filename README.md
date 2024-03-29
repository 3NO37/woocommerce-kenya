 
## ==== Description =====
 
Due to its vast size, both the country of Kenya and its capital city, Nairobi, cannot be considered as a single shipping zone. This poses a challenge to implementing varying prices for different regions. Moreover, the postal code feature cannot be relied upon as addressing in the country is poor, with few people having physical addresses that are often outdated or limited to P.O. Box numbers. It is recommended that Kenya be split into distinct shipping zones, similar to the approach taken in Nigeria and Angola. Similarly, Nairobi should be divided into smaller locations to allow for more accurate and efficient shipping calculations.

### === The Challenge ===

Coming up with custom code that would accomodate shipping to the different locations in Nairobi and outside Nairobi. Additionally, this locations will all have a different pricing when shipping to them.

### === Requirements ===

* WordPress 3.8 or greater
* PHP version 5.2.4 or greater
* MySQL version 5.0 or greater
* Code Snippets Plugin

### === The Code ===
```
/**
 * Adding or modifying shipping locations in Kenya
 */
add_filter( 'woocommerce_states', 'custom_woocommerce_states' );

function custom_woocommerce_states( $states ) {

  $states['KE'] = array(
    'KE001' => 'Langata Road - Nyayo Stadium', 
    'KE002' => 'Langata Road - Nairobi West',
	'KE003' => 'Langata Road - Madaraka',
	'KE004' => 'Langata Road - TMall',
	'KE005' => 'Langata Road - Wilson Airport',
	'KE006' => 'Langata Road - Langata',
	'KE007' => 'Langata Road - Galleria',
	'KE008' => 'Langata Road - Rongai',
	'KE009' => 'Langata Road - Kiserian',
	'KE010' => 'Mombasa Road - Nyayo Stadium',
	'KE011' => 'Mombasa Road - South C',
	'KE012' => 'Mombasa Road - South B',
	'KE013' => 'Mombasa Road - GM',
	'KE014' => 'Mombasa Road - Imara Daima',
	'KE015' => 'Mombasa Road - JKIA',
	'KE016' => 'Mombasa Road - Syokimau',
	'KE017' => 'Mombasa Road - Mlolongo',
	'KE018' => 'Mombasa Road - Sabaki',
	'KE019' => 'Mombasa Road - Athi River',
	'KE020' => 'Mombasa Road - Kitengela Town',
	'KE0107' => 'Juja Road - Mlango',
	'KE021' => 'Juja Road - Eastleigh',
	'KE023' => 'Juja Road - Huruma',
	'KE024' => 'Juja Road - Kariobangi',
	'KE025' => 'Juja Road - Dandora',
	'KE026' => 'Juja Road - Kayole',
	'KE027' => 'Jogoo Road - City Stadium',
	'KE028' => 'Jogoo Road - Rikana',
	'KE029' => 'Jogoo Road - Buruburu',
	'KE030' => 'Jogoo Road - Donholm',
	'KE031' => 'Jogoo Road - Umoja',
	'KE032' => 'Jogoo Road - Saika',
	'KE033' => 'Jogoo Road - Chokaa',
	'KE034' => 'Jogoo Road - Njiru',
	'KE035' => 'Jogoo Road - Ruai',
	'KE036' => 'Jogoo Road - Joska',
	'KE037' => 'Waiyaki Way - Chiromo',
	'KE038' => 'Waiyaki Way - Westlands',
	'KE039' => 'Waiyaki Way - ABC',
	'KE040' => 'Waiyaki Way - Kangemi',
	'KE041' => 'Waiyaki Way - Loresho',
	'KE042' => 'Waiyaki Way - Uthiru',
	'KE043' => 'Waiyaki Way - Kinoo',
	'KE044' => 'Waiyaki Way - Sigona',
	'KE045' => 'Waiyaki Way - Kikuyu',
	'KE046' => 'Waiyaki Way - Limuru',
	'KE047' => 'Waiyaki Way - Kileleshwa',
	'KE048' => 'Waiyaki Way - Kyuna',
	'KE049' => 'Limuru Road - Ngara',
	'KE050' => 'Limuru Road - Parklands',
	'KE051' => 'Limuru Road - Highridge',
	'KE052' => 'Limuru Road - Muthaiga',
	'KE053' => 'Limuru Road - Gigiri',
	'KE054' => 'Limuru Road - Runda',
	'KE055' => 'Limuru Road - Kitsuru',
	'KE056' => 'Limuru Road - Ruaka',
	'KE057' => 'Limuru Road - Ndenderu',
	'KE058' => 'Limuru Road - Banana',
	'KE059' => 'Limuru Road - Gachie',
	'KE060' => 'Kiambu Road - DCI',
	'KE061' => 'Kiambu Road - Muthaiga North',
	'KE062' => 'Kiambu Road - Ridgeways',
	'KE063' => 'Kiambu Road - Runda',
	'KE064' => 'Kiambu Road - Fourways',
	'KE065' => 'Kiambu Road - Thindigua',
	'KE066' => 'Kiambu Road - Kiambu Town',
	'KE067' => 'Ngong Road - Upperhill',
	'KE068' => 'Ngong Road - City Mortuary',
	'KE069' => 'Ngong Road - Adams Arcade',
	'KE070' => 'Ngong Road - Jamhuri',
	'KE071' => 'Ngong Road - Junction',
	'KE072' => 'Ngong Road - Lavington',
	'KE073' => 'Ngong Road - Hurlingham',
	'KE074' => 'Ngong Road - Kawangware',
	'KE075' => 'Ngong Road - Naivasha Road',
	'KE076' => 'Ngong Road - Satellite',
	'KE077' => 'Ngong Road - Racecourse',
	'KE078' => 'Ngong Road - Karen',
	'KE079' => 'Ngong Road - Kerarapon',
	'KE080' => 'Ngong Road - Bulbul',
	'KE081' => 'Ngong Road - Ngong Town',
	'KE082' => 'Thika Road - Ngara',
	'KE083' => 'Thika Road - Pangani',
	'KE084' => 'Thika Road - Muthaiga',
	'KE085' => 'Thika Road - Utalii',
	'KE086' => 'Thika Road - Alsop',
	'KE087' => 'Thika Road - Ruaraka',
	'KE088' => 'Thika Road - Roysambu',
	'KE089' => 'Thika Road - Kasarani',
	'KE090' => 'Thika Road - Mwiki',
	'KE091' => 'Thika Road - Githurai',
	'KE092' => 'Thika Road - Kahawa West',
	'KE093' => 'Thika Road - Zimmerman',
	'KE094' => 'Thika Road - Githurai 44',
	'KE095' => 'Thika Road - Jacaranda',
	'KE096' => 'Thika Road - Ruiru',
	'KE097' => 'Thika Road - Kimbo',
	'KE098' => 'Thika Road - Juja',
	'KE099' => 'Thika Road - Thika Town',
	'KE0100' => 'Eastern Bypass - City Cabanas',
	'KE0101' => 'Eastern Bypass - Taj Mall',
	'KE0102' => 'Eastern Bypass - Coca Cola',
	'KE0103' => 'Eastern Bypass - Nyayo Embakasi',
	'KE0104' => 'Eastern Bypass - Baraka Estate',
	'KE0105' => 'Eastern Bypass - Utawala',
	'KE0106' => 'Eastern Bypass - Githunguri Utawala',
	'KE0107' => 'Mombasa',
	'KE0108' =>'Kwale',
	'KE0109' =>'Kilifi',
	'KE0110' =>'Tana River',
	'KE0111' =>'Lamu',
	'KE0112' =>'Taita Taveta',
	'KE0113' =>'Garissa',
	'KE0114' =>'Wajir',
	'KE0115' =>'Mandera',
	'KE0116' =>'Marsabit',
	'KE0117' =>'Isiolo',
	'KE0118' =>'Meru',
	'KE0119' =>'Tharaka-Nithi',
	'KE0120' =>'Embu',
	'KE0121' =>'Kitui',
	'KE0122' =>'Machakos',
	'KE0123' =>'Makueni',
	'KE0124' =>'Nyandarua',
	'KE0125' =>'Nyeri',
	'KE0126' =>'Kirinyaga',
	'KE0127' =>'Murang’a',
	'KE0128' =>'Kiambu',
	'KE0129' =>'Turkana',
	'KE0130' =>'West Pokot',
	'KE0131' =>'Samburu',
	'KE0132' =>'Trans-Nzoia',
	'KE0133' =>'Uasin Gishu',
	'KE0134' =>'Elgeyo-Marakwet',
	'KE0135' =>'Nandi',
	'KE0136' =>'Baringo',
	'KE0137' =>'Laikipia',
	'KE0138' =>'Nakuru',
	'KE0139' =>'Narok',
	'KE0140' =>'Kajiado',
	'KE0141' =>'Kericho',
	'KE0142' =>'Bomet',
	'KE0143' =>'Kakamega',
	'KE0144' =>'Vihiga',
	'KE0145' =>'Bungoma',
	'KE0146' =>'Busia',
	'KE0147' =>'Siaya',
	'KE0148' =>'Kisumu',
	'KE0149' =>'Homa Bay',
	'KE0150' =>'Migori',
	'KE0151' =>'Kisii',
	'KE0152' =>'Nyamira'
  );

  return $states;
}
```


### === Test the Solution ===
* Add item to cart
* Proceed to check out
* Add location to DELIVER TO
* Make sure you fill in all the required fields
== See the price changing

You can test the solution by accessing this page [WooCommerce Checkout Test](https://techstars.co.ke/woocommerce/)
