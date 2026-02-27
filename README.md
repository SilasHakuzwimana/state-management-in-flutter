# State Management in Flutter
A comprehensive Flutter state management assignment comparing Provider, Riverpod, Bloc, and GetX. Includes handwritten explanations, applicability table, and detailed Provider implementation guide with code snippets.


# Flutter State Management Assignment - Year 3 CSE

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Provider](https://img.shields.io/badge/Provider-6A1B9A?style=for-the-badge&logo=flutter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## Assignment Overview

This repository contains my submission for the **Year 3 CSE Assignment** on Flutter State Management. The assignment explores four major state management approaches in Flutter development, comparing their use cases, advantages, and implementation patterns.

## Repository Contents

| File | Description |
|------|-------------|
| `Year_3_CSE_Assignment_1.pdf` | Complete assignment submission (handwritten + typed sections combined) |
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
- Accessing state via `Provider.of` and `Consumer`
- Updating state with `notifyListeners()`
- UI rebuild mechanism explained

## 🚀 Key Code Snippets

### State Class (Counter Model)
```dart
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
🛠️ How to View the Assignment
Clone the repository

bash
git clone https://github.com/yourusername/your-repo-name.git
Open the PDF

Navigate to Year_3_CSE_Assignment_1.pdf

Open with any PDF viewer

📝 Assignment Requirements Met
✅ Handwritten explanations (scanned/included in PDF)

✅ Handwritten applicability table

✅ Typed Provider implementation guide

✅ Code snippets included

✅ Single PDF file format

✅ GitHub repository submission

📚 Additional Resources
Flutter Provider Documentation

Riverpod Official Docs

Bloc Library

GetX Package

👨‍🎓 Student Information
Course: Year 3 Computer Science Engineering

Assignment: CSE Assignment 1 - State Management

Submission Date: [Insert Date]

Institution: [Your Institution Name]

📄 License
This project is submitted for academic purposes. All code snippets are for educational demonstration.
