curlit
======
Burp Python plugin to turn requests into curl commands.

Requires Jython 2.7

Should handle JSON/XML fine as well as other HTTP verbs.

Examples:

	curl -isk -X "GET" \
	-b "PHPSESSID=uknmkohe8kpqgcod2s4oc6soe2"
	"http://www.example.com:80/category.php?id=8"

Login POST to PayPal

	curl -isk -H "Content-Type: application/x-www-form-urlencoded" \
	-d "login_email=test%40test.com&login_password=test&submit.x=Log+In&browser_name=Firefox&browser_version=20&browser_version_full=20.0&operating_system=Mac&bp_mid=v%3D1%3Ba1%3Dna%7Ea2%3Dna%7Ea3%3Dna%7Ea4%3DMozilla%7Ea5%3DNetscape%7Ea6%3D5.0+%28Macintosh%29%7Ea7%3Dna%7Ea8%3Dna%7Ea9%3Dtrue%7Ea10%3Dna%7Ea11%3Dtrue%7Ea12%3DMacIntel%7Ea13%3Dna%7Ea14%3DMozilla%2F5.0+%28Macintosh%3B+Intel+Mac+OS+X+10.7%3B+rv%3A20.0%29+Gecko%2F20100101+Firefox%2F20.0%7Ea15%3Dtrue%7Ea16%3Dna%7Ea17%3Dna%7Ea18%3Dwww.paypal.com%7Ea19%3Dna%7Ea20%3Dna%7Ea21%3Dna%7Ea22%3Dna%7Ea23%3D2560%7Ea24%3D1440%7Ea25%3D24%7Ea26%3D1358%7Ea27%3Dna%7Ea28%3Dna%7Ea29%3Dna%7Ea30%3Dna%7Ea31%3Dna%7Ea32%3Dna%7Ea33%3Dna%7Ea34%3Dna%7Ea35%3Dna%7Ea36%3Dna%7Ea37%3Dna%7Ea38%3Dna%7Ea39%3Dna%7Ea40%3Dna%7Ea41%3Dna%7Ea42%3Dna%7E&bp_ks1=v%3D1%3Bl%3D4%3BDi0%3A1526Di1%3A80Ui0%3A39Ui1%3A16Di2%3A112Ui2%3A75Di3%3A84Ui3%3A66&bp_ks2=&bp_ks3=" \
	-X "POST" \
	-b "X-PP-SILOVER=name%3DLIVE6.WEB.1%26silo_version%3D880%26app%3Dslingshot%26TIME%3D2809762129; cwrClyrK4LoCV1fydGbAxiNL6iG=DZxUYqlalCZJ0pyVc_ehNkvPcyzBa5u6-fgeTc2U5dKh762bZeJjNu0Rv_MfQnDI0SkzWw7qCavYqZ9U5-0UBJIJ_16JpSyGs8O-eNb8APmOxq1K7tmGvdvjbShoU_8u1nYCsG%7cZWZCurs-FezuHR8lu8rOXBkuGXT03HJ-9jiMzkyMohJAhjKH5OBG3uOkmid6FTOAbLSfaG%7c2TXCBNdSfZy5EPq3TAOTZhdaKaQ42tH-0pceY8q-4kaeZ3dLvptZ9kI1SmqI7QgN34UGf0%7c1368488360; KHcl0EuY7AKSMgfvHl7J5E7hPtK=x82XPm2vWMyH4c7yoVWawZjpRrH-KEaZBPrVj-Dn2WoMwEsTFRuh3y60B-nrSjfM3JeEWR_o0Jo2UgBL; cookie_check=yes; consumer_display=USER_HOMEPAGE%3d0%26USER_TARGETPAGE%3d0%26USER_FILTER_CHOICE%3d0%26BALANCE_MODULE_STATE%3d1%26GIFT_BALANCE_MODULE_STATE%3d1%26LAST_SELECTED_ALIAS_ID%3d0%26SELLING_GROUP%3d1%26PAYMENT_AND_RISK_GROUP%3d1%26SHIPPING_GROUP%3d1%26HOME_VERSION%3d1%26FORGOT_BUTTON_ROLE%3d33%26MCE2_ELIGIBILITY%3d4294967295; Apache=10.74.8.61.1368488328467224; X-PP-SILOVER=name%3DLIVE6.WEB.1%26silo_version%3D880%26app%3Dslingshot%26TIME%3D2289668433; SPARTAJSESSIONID=ab4dafb6ac000; analytics=rAXZtyhkspoYqZTS1Zr9mcv3arruxcResmtPWzQeLItvYvm1GoxKOqBuju48v1Vu; SPARTAJSESSIONIDV2=mXOLSWDcOhPnk2xxRG.Iz7EhBTGSmA-g2No5CC1bfkC-9AE5uz48PuQUbLoNdiZ4nfzTZPpytto; ts=vreXpYrS%3D1463159934%26vteXpYrS%3D1368490957%26vr%3Da042f88d13e0a4a1ec032b73fffdaf41%26vt%3Da042f88d13e0a4a1ec032b73fffdaf40; s_sess=%20s_cc%3Dtrue%3B%20s_ppv%3D0%3B%20tr_p1%3Dmain%253Amktg%253Apersonal%253A%253Ahome%3B%20v31%3Dmain%253Amktg%253Apersonal%253A%253Ahome%3B%20lt%3Dsubmit.x%255Emain%253Amktg%253Apersonal%253A%253Ahome%3B%20s_sq%3Dpaypalglobal%253D%252526pid%25253Dmain%2525253Amktg%2525253Apersonal%2525253A%2525253Ahome%252526pidt%25253D1%252526oid%25253DLog%25252520In%252526oidt%25253D3%252526ot%25253DSUBMIT%3B; s_pers=%20s_fid%3D4685881C1C1BEA24-3FF7B139D2D47BA5%7C1431561158665%3B%20gpv_c43%3Dmain%253Amktg%253Apersonal%253A%253Ahome%7C1368490958669%3B%20gpv_events%3Dno%2520value%7C1368490958671%3B; navcmd=_login-run; login_email=test%40test.com; flow_back_cookie=; navlns=0.0; bn_u=1341323394142521421; aksession=1368489454~id=cookieNLGq3p2JFFNM/AX8w6arT98AZYtV/WQidJBRyx2VOAhrqekdiCNe4X3/H7SH/yqr0DxxMzTajslgtury7FUb6mna04JTIg53EyW2tRRCGcXU5dzbdwqeDmnv8c9KBZz7i6zxf9eUTeM=; tcs=main:mktg:personal::home|submit.x" \
	"https://www.paypal.com:443/us/cgi-bin/webscr?cmd=_login-submit"`
