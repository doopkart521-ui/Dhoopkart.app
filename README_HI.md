# DhoopKart – Fresh Flutter Starter

Yeh ek fresh Flutter starter project hai. Ismein Dark Brown + Gold theme, sample product catalogue, local cart, COD checkout demo, Seller Centre aur Admin Panel ke starter screens hain.

## Zaroori sach
- Abhi product list aur cart app ke andar local demo data hai.
- COD checkout abhi real order Firestore mein save nahi karta.
- Seller registration, seller approval, product upload, admin permissions aur delivery tracking abhi placeholders hain.
- Firebase initialization ka code hai, lekin Firebase Android configuration add karna zaroori hai.
- Is ZIP ko production-ready marketplace ya installable APK na samjhein.

## ZIP se project kaise banayein
1. ZIP extract karein.
2. Computer par Flutter SDK aur Android Studio install karein.
3. Terminal mein extracted `DhoopKart_Fresh` folder open karein.
4. Commands chalayein:

```bash
flutter create . --platforms=android
flutter pub get
flutter run
```

Agar `flutter create` existing files ko replace karne ka prompt de, `lib/` aur `pubspec.yaml` ko overwrite na hone dein.

## Firebase connect karna
1. Firebase Console mein apna `DhoopKart` project kholein.
2. FlutterFire CLI install karein.
3. Run karein:

```bash
dart pub global activate flutterfire_cli
flutterfire configure
```

4. Is starter ke `main.dart` mein `firebase_options.dart` import karke `Firebase.initializeApp(options: DefaultFirebaseOptions.currentPlatform)` use karein.
5. Android app ka package name Firebase Console mein register karein.

## Next development phase
- Firebase Auth: customer/seller login
- Firestore: users, sellerApplications, products, carts, orders
- Seller approval and role-based access
- Product images ke liye Firebase Storage
- COD order creation and seller delivery status
- Firestore Security Rules
- Real admin access ko client-side role check par depend na karein; trusted backend/rules use karein.

## Suggested Firestore collections
- `users`
- `sellerApplications`
- `products`
- `orders`
- `categories`
- `featuredBrands`

Har order mein customer, seller, items, total, paymentMethod=`COD`, orderStatus aur deliveryStatus jaise fields rakhein. Personal details ko public product documents mein store na karein.
