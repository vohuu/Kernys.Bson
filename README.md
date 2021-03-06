Kernys.Bson
===========

Simple BSON Encoder &amp; Decoder for C#


Just copy Kernys.Bson/SimpleBSON.cs to your project folder.

And Check it out below "Using Kernys.Bson" section !

Using Kernys.Bson
-------------------

Encoding is very easy!

```csharp
var obj = new BSONObject ();
obj["hello"] = 123;

obj["where"] = new BSONObject();
obj["where"]["Korea"] = "Asia";
obj["where"]["USA"] = "America";
obj["bytes"] = new byte[128];

byte []buf = SimpleBSON.Dump(obj);
Console.WriteLine (buf);
```

Decoding is much easier!
```csharp
BSONObject obj = SimpleBSON.Load(buf);

Console.WriteLine(obj["hello"]); // => 123
Console.WriteLine(obj["where"]["Korea"]); // => "Asia"
Console.WriteLine(obj["where"]["USA"]); // => "America"
Console.WriteLine(obj["bytes"].binaryValue); // => 128-length bytes
```

That's all!

Compatibility
-------------------

No need reflections.
Works very well with Unity 3.x/4.x and any .NET framework versions.

License
-------------------

Kernys.Bson is available under the MIT license.
