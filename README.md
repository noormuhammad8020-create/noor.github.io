# How I Connect My C# WPF App to a Cloud Database (Step-by-Step Guide)

I used to build desktop apps with local SQL Server databases. But users wanted their data synced across devices. So I switched to **MongoDB Atlas** — and it changed everything.

## Why Use MongoDB Atlas?

✅ No need to install SQL Server on every PC  
✅ Real-time sync across devices  
✅ Free $50 credit for new accounts  
✅ Easy C# driver integration

## Step 1: Create Your Free Cluster
Go to [MongoDB Atlas](https://www.mongodb.com/atlas) and sign up.

## Step 2: Get Your Connection String
- Click "Connect"
- Choose "C#" as your driver
- Copy the connection string

## Step 3: Use It in Your WPF App

```csharp
using MongoDB.Driver;

var client = new MongoClient("your-connection-string-here");
var database = client.GetDatabase("MyWpfApp");
var collection = database.GetCollection<BsonDocument>("UserData");
```

> 💡 **Disclosure**: If you sign up using my link below, I may earn a small commission at no extra cost to you. Thank you for supporting my work!

👉 [Get $50 Free Credit on MongoDB Atlas](https://partnerstack.com/partner/mongodb)

This solution works great for offline-first WPF apps with cloud backup. Hope it helps you too!
