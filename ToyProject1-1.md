`````````
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});
  
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'ToDoList',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.lightGreen.shade200),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'ToDoList'),
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
  /*int _counter = 0;

  void _incrementCounter() {
    setState(() {
      _counter++;
    });
  }
*/
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.lightGreen.shade200,
      appBar: AppBar(
        centerTitle: true,
        leading: const Icon(
          Icons.calendar_view_day,
          size: 30,
        ),
        title: const Text(
        "ToDoList",
          style: TextStyle(
            fontSize: 27,
            fontWeight: FontWeight.w500,
          ),
      ),
        actions: [
          IconButton(
            icon: const Icon(
              Icons.add,
              size: 30,
            ), onPressed: () {  },
          )
        ],
      ),
      body: const Column(
        children: [
          ExpansionTile(title: Text(
          "오늘의 할 일",
        style: TextStyle(
          fontSize: 20,
        ),
      ),),
          ExpansionTile(title: Text(
            "일주일 간 해야할 일",
            style: TextStyle(
              fontSize: 20,
            ),
          ),),
          ExpansionTile(title: Text(
            "이번 달의 할 일",
            style: TextStyle(
              fontSize: 20,
            ),
          ),),
          ExpansionTile(title: Text(
            "지금 할 일",
            style: TextStyle(
              fontSize: 20,
            ),
          ),),
          ExpansionTile(title: Text(
            "오늘의 할 일",
            style: TextStyle(
              fontSize: 20,
            ),
          ),),
        ],
      ),
    );
  }
}
```````````
