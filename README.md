# Flutter State Management Assignment 1 - Year 3 CSE

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Provider](https://img.shields.io/badge/Provider-6A1B9A?style=for-the-badge&logo=flutter&logoColor=white)
![Riverpod](https://img.shields.io/badge/Riverpod-DB3552?style=for-the-badge&logo=flutter&logoColor=white)
![Bloc](https://img.shields.io/badge/Bloc-FF9800?style=for-the-badge&logo=flutter&logoColor=white)
![GetX](https://img.shields.io/badge/GetX-8E44AD?style=for-the-badge&logo=flutter&logoColor=white)

A comprehensive Flutter state management assignment comparing Provider, Riverpod, Bloc, and GetX. Includes handwritten explanations, applicability table, and detailed Provider implementation guide with code snippets.



## Assignment Overview

This repository contains my submission for the **Year 3 CSE Assignment** on Flutter State Management. The assignment explores four major state management approaches in Flutter development, comparing their use cases, advantages, and implementation patterns.

## Repository Contents

| File | Description |
|------|-------------|
| `Assignment #1 - 223001019.pdf` | Complete assignment submission (handwritten + typed sections combined) |
| `README.md` | This documentation file |

## Assignment Questions Covered

### 1. State Management Explanations (Handwritten)
Brief explanations of four state management solutions:
- **Provider** - Google-recommended wrapper around InheritedWidget
- **Riverpod** - Compile-safe provider with improved syntax
- **Bloc** - Event-driven business logic component pattern  
- **GetX** - Micro-framework with reactive state management

### 2. Applicability Matrix (Handwritten)
A comprehensive table matching state management solutions to project scenarios:

| Situation | Recommended Solution |
|-----------|---------------------|
| Small applications | Provider / GetX |
| Medium applications | Provider / Riverpod |
| Large/Enterprise | Bloc / Riverpod |
| Team projects | Bloc / Riverpod |
| Fast development | GetX |
| Strict architecture | Bloc |

### 3. Provider Implementation Guide (Typed)
Detailed step-by-step explanation of Provider with code snippets:
- Adding dependency to `pubspec.yaml`
- Creating a state class with `ChangeNotifier`
- Providing state using `ChangeNotifierProvider`
- Accessing state via `context.watch<T>()`, `context.read<T>()`, `Provider.of<T>(context)`,  and `Consumer<T>`
- Updating state with `notifyListeners()`
- UI rebuild mechanism explained

## Key code snippets

### State Class (Counter Model)

```bash
class Counter with ChangeNotifier {
  int _count = 0;
  int get count => _count;
  
  void increment() {
    _count++;
    notifyListeners();
  }
}
Providing State
dart
void main() {
  runApp(
    ChangeNotifierProvider(
      create: (context) => Counter(),
      child: const MyApp(),
    ),
  );
}
Accessing State
dart
// Using Provider.of
final counter = Provider.of<Counter>(context);
Text('${counter.count}')

// Using Consumer
Consumer<Counter>(
  builder: (context, counter, child) {
    return Text('${counter.count}');
  },
)
```
## How to View the Assignment

Clone the repository

```bash
git clone https://github.com/SilasHakuzwimana/state-management-in-flutter.git
```
## Open the PDF

1. Navigate to Assignment #1 - 223001019.pdf
2. Open with any PDF viewer

## Assignment Requirements Met

1. Handwritten explanations (scanned/included in PDF)
2. Handwritten applicability table
3. Typed Provider implementation guide
4. Code snippets included
5. Single PDF file format
6. GitHub repository submission

## Additional Resources

1. Flutter Provider Documentation
2. Riverpod Official Docs
3. Bloc Library
4. GetX Package

## Student Information

Course details: Year 3 Computer Engineering - Mobile Application Systems and Design
Assignment: CSE Assignment 1 - State Management in Flutter
Student name & Reg. Number: Silas HAKUZWIMANA - 223001019
Submission Date: 27th February 2026
Institution: UR-CST

## License

This project is submitted for academic purposes. All code snippets are for educational demonstration.
