# 🌍 GeoNames SwiftUI App

This is a SwiftUI iOS app that fetches and displays a list of the top 10 most populous cities within a defined bounding box using the [GeoNames](http://www.geonames.org/) API. When a city is tapped, the app navigates to a map view showing the city's location.

---

## 🚀 Features

- Fetches city data via the GeoNames RESTful JSON API
- Lists city name, country code, and population
- Displays selected city on a map
- Supports iOS 17+ with the latest MapKit APIs (`Map` and `Marker`)

---

## 🧱 Tech Stack

- SwiftUI
- Combine / ObservableObject
- MapKit (iOS 17+ compatible)

---

## 📸 Screenshots

| City List Screen    | City Map View            |
| ------------------- | ------------------------ |
| Shows top 10 cities | Zoomable map with marker |

---

## 🧪 Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/geonames-swiftui-app.git
   cd geonames-swiftui-app
   ```

2. **Open in Xcode:**

   ```
   open GeoNamesApp.xcodeproj
   ```

3. **Add your GeoNames username** in `CityViewModel.swift`:

   ```swift
   let username = "your_username_here"
   ```

4. **Allow HTTP calls** by ensuring your `Info.plist` includes:

   ```xml
   <key>NSAppTransportSecurity</key>
   <dict>
       <key>NSExceptionDomains</key>
       <dict>
           <key>geonames.org</key>
           <dict>
               <key>NSIncludesSubdomains</key>
               <true/>
               <key>NSTemporaryExceptionAllowsInsecureHTTPLoads</key>
               <true/>
               <key>NSTemporaryExceptionMinimumTLSVersion</key>
               <string>TLSv1.1</string>
           </dict>
       </dict>
   </dict>
   ```

5. **Build and Run!** 🎉

---

## 🌐 API Reference

GeoNames Cities Web Service: [http://api.geonames.org/citiesJSON](http://api.geonames.org/export/web-services.html#citiesJSON)

**Example:**

```
http://api.geonames.org/citiesJSON?north=44.1&south=-9.9&east=-22.4&west=55.2&username=demo
```

---

## 📄 License

MIT License. Feel free to fork and enhance!

---

## 🙋‍♂️ Author

👨‍💻 Aayush Swami — Student at ASU, App created for CSE 335 Lab 6

