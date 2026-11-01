BGP TEST - COMPLETE GITHUB PAGES PACK
=====================================

Is ZIP mein GitHub Pages ke liye poora website source root folder mein rakha gaya hai.
Yeh sirf update/patch ZIP nahi hai. Logo, HTML, CSS, JavaScript, Supabase config,
SQL setup, question folders aur Hindi guide sab shamil hain.

1) GITHUB PAR UPLOAD
--------------------
1. GitHub par New repository banayein, jaise: bgp-test
2. Is ZIP ko extract karein.
3. Extract hone ke baad BGP_TEST_GITHUB_COMPLETE folder ke ANDAR ki sabhi files
   (index.html, app.js, style.css, assets, database, questions, etc.) repository
   ke root mein upload karein. Folder ko dobara andar folder ke roop mein upload na karein.
4. Repository > Settings > Pages kholein.
5. Build and deployment mein Deploy from a branch chunein.
6. Branch: main, Folder: /(root), Save.
7. GitHub Pages URL banne par usse open karein.

2) SUPABASE DATABASE
--------------------
1. Supabase project ke SQL Editor mein database/setup.sql ka poora SQL run karein.
2. Agar pehle se purana BGP TEST database bana hua hai, to records delete na karein.
   Pehle database/upgrade_v2.sql ko review karke run karein. Existing data ka backup rakhein.
3. Supabase Storage mein daily-homework bucket aur app ke zaroori storage buckets/policies
   README ya SQL ke anusaar configure karein.
4. Project Settings > API se Project URL aur Publishable/anon key lekar
   supabase-config.js mein set karein.
5. Browser mein kabhi service_role/secret key mat rakhein.

3) QUESTION JSON
----------------
Questions ko database mein rakhne ki jagah questions/ ke subject folder mein JSON file
rakhein. Udaharan: questions/science/chapter-1.json
Expected format questions/README.txt mein diya gaya hai.
Is pack mein question folders taiyar hain; actual question bank files tabhi shamil hongi
jab aap apne questions denge.

4) PROFILE PHOTO AUR SUBJECT FOLDERS
---------------------------------
- Profile photo button se phone gallery open hoti hai (image/*).
- PNG/JPG/WebP image browser mein 256px ke aas-paas resize hokar chhoti JPEG (target ~100 KB) banegi.
- Har mobile number ke liye wahi profile.jpg replace hoti hai, isliye baar-baar nayi file jama nahi hogi.
- Is overwrite ke liye upgrade_v2.sql dobara run karein, jisse Storage UPDATE policy bhi add ho.
- Notes tab mein pehle Subject folders, phir us subject ke PDFs dikhte hain.
- Class tab mein Class > Subject folders > Chapter list dikhti hai.

5) IMPORTANT
------------
- Yeh static frontend GitHub Pages par host hota hai; data Supabase se aata hai.
- GitHub Pages upload se Supabase tables, policies ya Storage apne-aap configure nahi hote.
- Admin access ko production mein secure karne ke liye Supabase Auth aur proper RLS policies
  configure karna zaroori hai. Sirf browser mein mobile-number check ko secure authentication
  na samjhein.
- App ko aapke live Supabase project par end-to-end test nahi kiya gaya hai.
