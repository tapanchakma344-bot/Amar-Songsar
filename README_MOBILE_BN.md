# আমার সংসার — মোবাইল থেকে APK Build

## কী আছে
- বাংলা Android starter app
- আয়/খরচ যোগ এবং স্থানীয় ফোনে সংরক্ষণ
- GitHub Actions workflow, যা স্বয়ংক্রিয়ভাবে debug APK তৈরি করে

## Redmi ফোন থেকে APK তৈরি
1. GitHub অ্যাকাউন্টে লগইন করুন।
2. নতুন repository তৈরি করুন, নাম `amar-songsar` দিন।
3. এই ZIP Extract করে এর ভেতরের সব ফাইল repository-তে upload করুন। `.github/workflows/build-apk.yml` ফাইলটিও অবশ্যই upload হতে হবে।
4. Commit changes করুন।
5. Repository-র Actions ট্যাবে যান।
6. `Build Amar Songsar APK` workflow নির্বাচন করে `Run workflow` চাপুন (অথবা push-এর পর workflow নিজে চলবে)।
7. Build সফল হলে workflow run খুলুন; নিচের Artifacts অংশ থেকে `amar-songsar-debug-apk` ডাউনলোড করুন।
8. ZIP extract করে `app-debug.apk` ফাইলটি Redmi ফোনে ইনস্টল করুন। Android চাইলে ওই উৎস থেকে Install unknown apps অনুমতি দিন।

## গুরুত্বপূর্ণ সীমাবদ্ধতা
এটি এখনো প্রাথমিক অফলাইন সংস্করণ। হিসাব এই ফোনে সংরক্ষিত হয়। মোবাইল নম্বর-পাসওয়ার্ড লগইন, পরিবারের একাধিক সদস্য, ক্লাউড ব্যাকআপ/সিঙ্ক, আমন্ত্রণ কোড ও ভূমিকা-নিয়ন্ত্রণ এখনো বাস্তবায়িত হয়নি। এগুলো যোগ করার আগে Firebase Authentication ও Cloud Firestore এবং যথাযথ নিরাপত্তা নিয়ম সেটআপ করতে হবে।
