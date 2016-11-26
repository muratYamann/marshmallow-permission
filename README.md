# marshmallow-permission-
Android 6.0 izinleri







//-----------MarsMallow Permission---------------------------------------------


      /*
       getPermissionCallPhone();
       getPermissionSendSms();
       getPermissionToInternet();
       getPermissionLocation();
       */


       /**
        <uses-permission android:name="android.permission.BLUETOOTH" />
        <uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />
        <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
        <uses-permission android:name="android.permission.INTERNET" />
        <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
        <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
        <uses-permission android:name="android.permission.CALL_PHONE" />
        * */


   final static int PERMISSIONS_REQUEST_CODE = 1;


   public void getPermissionBluetooth() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.BLUETOOTH)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.BLUETOOTH)) {
           }
           requestPermissions(new String[]{Manifest.permission.BLUETOOTH},
                   PERMISSIONS_REQUEST_CODE);
       }
   }




   public void getPermissionBluetoothAdmin() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.BLUETOOTH_ADMIN)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.BLUETOOTH_ADMIN)) {
           }
           requestPermissions(new String[]{Manifest.permission.BLUETOOTH_ADMIN},
                   PERMISSIONS_REQUEST_CODE);
       }
   }




   public void getPermissionWriteExternalStorage() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.WRITE_EXTERNAL_STORAGE)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.WRITE_EXTERNAL_STORAGE)) {
           }
           requestPermissions(new String[]{Manifest.permission.WRITE_EXTERNAL_STORAGE},
                   PERMISSIONS_REQUEST_CODE);
       }
   }


   public void getPermissionToInternet() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.INTERNET)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.INTERNET)) {
           }
           requestPermissions(new String[]{Manifest.permission.INTERNET},
                   PERMISSIONS_REQUEST_CODE);
       }
   }


   public void getPermissionAccessNetworkState() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.ACCESS_NETWORK_STATE)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.ACCESS_NETWORK_STATE)) {
           }
           requestPermissions(new String[]{Manifest.permission.ACCESS_NETWORK_STATE},
                   PERMISSIONS_REQUEST_CODE);
       }
   }


   public void getPermissionLocation() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.ACCESS_FINE_LOCATION)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.ACCESS_FINE_LOCATION)) {
           }
           requestPermissions(new String[]{Manifest.permission.ACCESS_FINE_LOCATION},
                   PERMISSIONS_REQUEST_CODE);
       }
   }




   public void getPermissionCallPhone() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.CALL_PHONE)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.CALL_PHONE)) {
           }
           requestPermissions(new String[]{Manifest.permission.CALL_PHONE},
                   PERMISSIONS_REQUEST_CODE);
       }
   }


   public void getPermissionSendSms() {
       if (ContextCompat.checkSelfPermission(this, Manifest.permission.SEND_SMS)
               != PackageManager.PERMISSION_GRANTED) {


           if (shouldShowRequestPermissionRationale(
                   Manifest.permission.SEND_SMS)) {
           }
           requestPermissions(new String[]{Manifest.permission.SEND_SMS},
                   PERMISSIONS_REQUEST_CODE);
       }
   }
  
 
  @Override
   public void onRequestPermissionsResult(int requestCode,
                                          @NonNull String permissions[],
                                          @NonNull int[] grantResults) {
       if (requestCode == PERMISSIONS_REQUEST_CODE) {
           if (grantResults.length == 1 &&
                   grantResults[0] == PackageManager.PERMISSION_GRANTED) {
               Toast.makeText(this, "permission granted", Toast.LENGTH_SHORT).show();
           } else {
               Toast.makeText(this, "permission denied", Toast.LENGTH_SHORT).show();
           }
       } else {
           super.onRequestPermissionsResult(requestCode, permissions, grantResults);
       }
   }










