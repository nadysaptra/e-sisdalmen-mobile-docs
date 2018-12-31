# Notification
Do not use fcm using `notifications` param when sending fcn from backend, instead using `data`.
After receiving notification from fcm, use localNotification to show each notif to user

## GCM / FCM Key
> GCM / Fcm key  were setup on `App.js`

> you can change gcm key to your need in https://console.firebase.google.com

> go to your app `settings`

> go to `Cloud Messaging` tab

> copy and paste `Sender ID` to App.js > senderID parameter


## Example on Receiving notification from FCM
```
_handleNotificationOpen = (notif) => {
this._scheduleCheckingNotification(notif)
if (!notif.userInteraction) { 
    // when received fcm
    this.pushNotification.setApplicationIconBadgeNumber(0);
} else {
    // when clicking on notification
    if (notif.param === 'progress' && notif.param_id) {
        Actions.push('detail-pekerjaan', { progressid: notif.param_id })
    }
    if (notif.param === 'message' && notif.param_id) {
        Actions.push('progress-message', { progressid: notif.param_id })
    }
}
// required on iOS only (see fetchCompletionHandler docs: 
notif.finish(PushNotificationIOS.FetchResult.NoData);
}
```

