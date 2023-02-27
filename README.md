

## Features

You can pretty the JSON in String state

Image:
![MarineGEO circle logo](https://raw.githubusercontent.com/Usmoxan/usmoxan.github.io/main/example_image.jpg "MarineGEO logo")



## Usage

You can pretty the JSON in String state

## EXAMPLE CODE

```dart
import 'package:flutter/material.dart';
import 'package:json_pretty/json_pretty.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo Json Pretty',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: const MyHomePage(title: 'Home Page'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  var dataJson =
      """{"borrowers":[{"name":"Zuhriddin","loans":[{"amount":12000,"dateBorrowed":"_dateBorrowed","datePaid":"_datePaid"},{"amount":5000,"dateBorrowed":"2022","datePaid":"232323"}]},{"name":"Usmoxan","loans":[{"amount":122000,"dateBorrowed":"_dateBorrowed","datePaid":"_datePaid"},{"amount":200,"dateBorrowed":"2022","datePaid":"232323"}]}]}""";
  String prettyJson = 'Please Click Floating Action Button \n\n\n';
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: ListView(
          children: <Widget>[
            Text(
              prettyJson + dataJson,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          setState(() {
            prettyJson = prettyPrintJson(dataJson);
          });
        },
        tooltip: 'Pretty Json Text',
        child: const Icon(Icons.done_all),
      ),
    );
  }
}

```

## Additional information

Its easy.