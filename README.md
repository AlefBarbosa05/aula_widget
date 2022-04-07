# aula_widget

import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Column(children: [
      Row(children: [
        
        meuContainer ('A', Colors.blue, 80),
        meuContainer ('A', Colors.blue, 80),
        meuContainer ('A', Colors.blue, 80),
        
      ]),
      Row(children: [
        meuContainer ('A', Colors.blue, 80),
        meuContainer ('A', Colors.blue, 80),
        meuContainer ('A', Colors.blue, 80),
      ])

    ]);
  }
}


meuContainer (String nome, Color cor, double largura){
  
  return Container(
          margin: const EdgeInsets.all(10.0),
          color: Colors.blue,
          width: largura,
          height: 48.0,
          child: Text(nome));
 }
