# webdev_helloworld

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

To create a Flutter project inside Visual Studio Code, first you have to have:

	1. Visual Studio Code installed
	2. Flutter SDK installed 
	3. Flutter and Dart plugin installed 
	4. Enable flutter for web
	
Once you finish, it will set you up with some starting code. The starting code is created by Flutter team,
and all it does is it creates a simple counter app. Now, in this case it is a counter app created by using a Scaffold.
If you want to quickly run it and see what it looks like, simply open the terminal. To open a terminal in Visual Studio,
just go ahead at left top of your screen and click on open terminal 

Now in order to run this code, on the terminal, type flutter run -d chrome 
-d here stands for device id

and once it is done, this is what you should see. A really simple application with top bar, a floating button to increment the counter that you can press. 

Now, in order to understand I am actually gonna delete everything that is currently inside the file, other than the top two lines.

void main() {
  runApp(MyApp());
}

Now, we will get a little error here, if you see it in dart analysis where it says 

"The function 'MyApp' isn't defined.
Try importing the library that defines 'MyApp', correcting the name to the name of an existing function, or defining a function named 'MyApp'."

Well that is because 'MyApp' is actually the Flutter team's app, it was the counter app. Because we already delete it, so MyApp doesn't exist anymore. So in this we will delete it.

So instead, the app we are gonna run is a blank MaterialApp.

void main() {
  runApp(MaterialApp());
}

 MaterialApp is something that can form the material design pattern. Material design is just a design style or a concept that was created by Google and a lot of startup and companies adopted it for their web application. Inside the MaterialApp, the most important thing that you need to set is the home and this is where evertything starts. 

void main() {
  runApp(MaterialApp(home: ,));
}

If we go ahead and say that, in the home of the app what we want to see is simply the text widget and this text just says Hello World. 

void main() {
  runApp(MaterialApp(home: Text('Hello World'),));
}

Now, if we go ahead, and run this app, you will see the text show up inside our material app. But at the moment, it doesn't look great. It is just a blank screen with some red texts. But it does say what we wanted to say which is Hello World. 

We have started building our widget tree. And it is really a simple one. It is only got two widgets. The first parent widget is the MaterialApp widget.

The next thing we are saying inside this MaterialApp is, the thing that we want to show is the text widgets in the middle. By default, text the widget get aligned to the top left corner.

So in order to get our Texts alligned to the center, we will use a center widget. Inside the center widget, we will put our text widget. We got 3 widgets now if you realized. 

Now, I will just remove the text widget for awhile, inside the home we are going to put a center wiget

void main() {
  runApp(MaterialApp(home: Center(),));
}

A Center widget can have a child 

void main() {
  runApp(MaterialApp(home: Center(child: ,),));
}

And its child is going to be our text widget

void main() {
  runApp(MaterialApp(home: Center(child: Text('Hello World'),),));
}

Now if I click on my terminal here and press "r" key on keyboard for hot reload, you should see the text widget is now centered. 

This is the starting point of creating Flutter Web App is to create a Hello World web page.

The Flutter team advices that; whenever you creating a widget which usually involves the
paranthesis { } and round bracket ( ) 

void main() {
  runApp(MaterialApp(home: Center(child: Text("Hello"))));
  }
 
just add a coma , after it

void main() {
  runApp(MaterialApp(home: Center(child: Text("Hello"),),),);
  }

When I right click (mouse), and click on reformat code, it will automatically turn my one line of codes which is
very difficult to recognize code into an indentive structure 

void main() {
  runApp(
    MaterialApp(
      home: Center(
        child: Text("Hello World"),
      ),
    ),
  );
}

Now, this thing called main () is important. Everything lies inside this main () method. If you are from Java and Kotlin programming background, Flutter needs to have the main method or the main function (), just like Java and Kotlin. If there is no main () it has no idea where to start. Every time you run the app, the starting file is called main.dart 


