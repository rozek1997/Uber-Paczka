# Uber-Paczka

Project inspired by Uber but moved to world of package delivery. Anyone can order a package to be delivered within an hour in town. You order we deliver


## Technology used

* Android SDK v28
* Firebase Authentication
* Firebase Firestore
* Google Maps API 
* Google Distance Matrix API


## Views

<table cellpadding="0" cellspacing="5" style="border: none">
<tr>
<th>
    <h3>Splash screen</h3>
</th>
<th>
    <h3>Login screen</h3>
</th>
<th>
<h3> Main screen</h3>
</th>
</tr>
<tr>
<td>

![splassh-screen](https://user-images.githubusercontent.com/38226876/76958575-4c646180-6918-11ea-88dc-e00623580d37.jpg "Splash screen")

</td>
<td>

![login](https://user-images.githubusercontent.com/38226876/76959014-078cfa80-6919-11ea-8c83-e93aa50baead.jpg "Login")

</td>
<td>

![main-view](https://user-images.githubusercontent.com/38226876/76958562-48384400-6918-11ea-8b12-0012c46bc550.jpg)

</td>
</tr>
<tr>
<th>
    <h3>Order screen</h3>
</th>
<th>
    <h3>Summary screen</h3>
</th>
<th>
<h3>Side menu</h3>
</th>
</tr>
<tr>
<td>

![order](https://user-images.githubusercontent.com/38226876/76962340-550c6600-691f-11ea-9802-ff02cb453961.png)
</td>
<td>

![summary-screen](https://user-images.githubusercontent.com/38226876/76958871-c0066e80-6918-11ea-9442-426aea02d3dc.png)

</td>
<td>

![side-bar](https://user-images.githubusercontent.com/38226876/76959342-b29db400-6919-11ea-85f0-28e1510ce6b1.jpg)

</td>
</tr>
<tr>
<th>
<h3>Internet error</h3>
</th>
</tr>

<tr>
<td>

![internet-error](https://user-images.githubusercontent.com/38226876/76958554-45d5ea00-6918-11ea-805b-0d2307cc3d05.jpg)

</td>
</tr>
</table>

## Architecture overview

The application does not use the thrid party API to retrieve user information. This means that each user has to go through the registration process to provide their basic data. Additionally, if the user wants to become a driver delivering packages, it is required to provide additional information
Local data is in effect immutable, the client just downloads updated
versions of data as needed. Local data is only modified as a result of
api operations.

The application uses mainly fragments, because activities are quite heavy for the system. To improve the user experience, the application uses GPS to track the current location of the user. The user must agree to use his location data.

## Authentication & security

All confidential information is stored in Firebase Authentication service. This includes credit card numbers, telephone numbers etc. The rest of the information such as your home address is stored in Firestore.
Logging in to the application is done by e-mail and password. You do not need to provide this information every time you log on. Logging in is done using token and refresh token.

