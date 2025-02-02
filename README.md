# DatapassingMethods

import 'package:chatapp/config/pagePath.dart';
import 'package:chatapp/config/themes.dart';
import 'package:flutter/material.dart';
import 'package:get/get.dart';

import 'View/homepage/hhh.dart';
import 'View/welcome/welcomepage.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return GetMaterialApp(
      getPages: pagePath,
      title: 'ChatApp',
      theme: lightTheme,
      darkTheme: darkTheme,
      // themeMode: ThemeMode.system,
      themeMode: ThemeMode.dark,
      home: HomePageScreen(),
      // home: Welcomepage(),
    );
  }
}



======================================
import 'package:chatapp/View/Auth/authpage.dart';
import 'package:chatapp/View/homepage/hhh.dart';
import 'package:get/get.dart';

import '../View/Auth/widget/ChatpageDetails.dart';

var pagePath = [
  GetPage(
    name: "/authPage",
    page: () => Authpage(),
    transition: Transition.downToUp,
    transitionDuration: Duration(milliseconds: 500),
  ),
  GetPage(
    name: "/homePage",
    page: () => HomePageScreen(),
    transition: Transition.leftToRight,
    transitionDuration: Duration(milliseconds: 500),
  ),
  GetPage(
    name: "/chatPageDetails",
    page: () => ChatpageDetails(),
    transition: Transition.rightToLeft,
    transitionDuration: Duration(milliseconds: 500),
  ),
];


