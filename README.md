import 'package:flutter/material.dart';

void main() => runApp(new MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new MaterialApp(
      title: 'Login Animation',
      home: new LoginPage(),
    );
  }
}

class LoginPage extends StatefulWidget {
  const LoginPage({Key key}) : super(key: key);
  @override
  _LoginPageState createState() => new _LoginPageState();
}

class _LoginPageState extends State<LoginPage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Container(
        decoration: BoxDecoration(
            image: DecorationImage(
                image: NetworkImage(
                    "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS-CwDJB5lOY6jSCrHGW0WhDUHXSKmuOnCc2eZoAFzSrIkoNvzwQOvl-i1-pZZRYxHdsLQ&usqp=CAU"),
                fit: BoxFit.cover)),
        child: Container(
          decoration: BoxDecoration(
              gradient: LinearGradient(
            colors: [
              Color.fromRGBO(162, 146, 199, 0.8),
              Color.fromRGBO(51, 51, 63, 0.9)
            ],
            begin: FractionalOffset.topCenter,
            end: FractionalOffset.bottomCenter,
          )),
          child:
              ListView(padding: const EdgeInsets.all(0.0), children: <Widget>[
            Stack(
              alignment: AlignmentDirectional.bottomCenter,
              children: <Widget>[
                Column(
                  children: <Widget>[
                    Padding(
                      padding: const EdgeInsets.only(top: 270.0),
                    ),
                    Container(
                      padding: const EdgeInsets.all(10.0),
                      child: Column(
                        children: <Widget>[
                          Padding(
                              padding: const EdgeInsets.all(
                            10.0,
                          )),
                          TextField(
                            decoration: InputDecoration(
                                icon: Icon(
                                  Icons.person_outline,
                                  color: Colors.white,
                                ),
                                hintText: "Username"),
                          ),
                          Padding(
                              padding: const EdgeInsets.all(
                            10.0,
                          )),
                          TextField(
                            decoration: InputDecoration(
                                icon: Icon(
                                  Icons.lock_outline,
                                  color: Colors.white,
                                ),
                                hintText: "Password"),
                          ),
                          FlatButton(
                            padding:
                                const EdgeInsets.only(top: 220.0, bottom: 30.0),
                            onPressed: null,
                            child: Text(
                              "dont have an account? Sign Up here",
                              style: TextStyle(
                                  fontSize: 12.0,
                                  color: Colors.white,
                                  fontWeight: FontWeight.w300,
                                  letterSpacing: 0.5),
                            ),
                          )
                        ],
                      ),
                    )
                  ],
                ),
                new SignIn()
              ],
            )
          ]),
        ),
      ),
    );
  }
}

class SignIn extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new Padding(
      padding: const EdgeInsets.all(60.0),
      child: new Container(
        alignment: FractionalOffset.center,
        width: 320.0,
        height: 60.0,
        decoration: BoxDecoration(
            borderRadius: BorderRadius.all(const Radius.circular(30.0))),
        child: Text(
          "Sign In",
          style: TextStyle(
              color: Colors.white,
              fontSize: 20.0,
              fontWeight: FontWeight.w300,
              letterSpacing: 0.3),
        ),
      ),
    );
  }
}
