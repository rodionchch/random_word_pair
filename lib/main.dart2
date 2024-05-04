import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // Этот виджет является корневой папкой вашего приложения.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.blue.shade200),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});

  // Этот виджет является домашней страницей вашего приложения. Он отслеживает состояние, что означает
  // что у него есть объект State (определение приведено ниже), который содержит поля, влияющие на
  // его внешний вид.

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      // Этот вызов setState сообщает платформе Flutter framework, что
      // в этом состоянии что-то изменилось, что заставляет ее повторно запустить метод построения
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    // Этот метод запускается повторно при каждом вызове setState, например, как это сделано
    // с помощью метода _incrementCounter, описанного выше.
    //
    // Платформа Flutter была оптимизирована для упрощения повторного запуска методов сборки
    // быстро, так что вы можете просто перестроить все, что нуждается в обновлении, а не изменять экземпляры виджетов по отдельности.
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        // Здесь мы берем значение из объекта MyHomePage, который был создан с помощью
        // метода App.build, и используем его для установки заголовка нашей панели приложений.
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          // ПОПРОБУЙТЕ ЭТО: вызовите "debug painting" (выберите "Переключить Debug Paint"
          // действие в среде IDE или нажмите "p" в консоли), чтобы увидеть
          // структуру для каждого виджета.
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            const Text(
              'You have pushed the button this many times:',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.headlineMedium,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ),
    );
  }
}
