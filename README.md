# Projeto Flutter com Firebase

Este guia descreve os passos necessários para configurar um projeto Flutter integrado ao Firebase Firestore, baseado em experiências e ajustes após testes.

## Passos para Configuração

### 1. Criar o Projeto Flutter
- Abra o Visual Studio Code.
- Use o atalho `Ctrl + Shift + P` e selecione `Flutter: New Project`.

### 2. Criar um Projeto no Firebase
- Acesse o Firebase Console.
- Crie um novo projeto, mas **não adicione nenhuma linha de código** sugerida pelo Firebase no seu projeto Flutter.

### 3. Criar um Banco de Dados Firestore
- No Firebase Console, crie um novo banco de dados Firestore.

### 4. Instalar Dependências
- Pesquise no Google o nome das dependências e acesse o site pub.dev.
- Instale as dependências:
  ```sh
  flutter pub add cloud_firestore
  flutter pub add firebase_core
- Importe as dependências no main.dart:
  ```sh
  import 'package:cloud_firestore/cloud_firestore.dart';
  import 'package:firebase_core/firebase_core.dart';
### 5. Adicionar Nome/ID do package
- Adicionar nome/ID do package caso não houver em android/app/src/main/AndroidManifest.xml
  ```sh
  <manifest xmlns:android="http://schemas.android.com/apk/res/android" package="com.example.NOME_QUE_EU_QUISER">

### 6. Verifica se o Node.js está instalado, senão instalar:
    ```bash
    node --version
    ```

### 7. Verifica se o npm está instalado, senão instalar:
    ```bash
    npm --version
    ```

### 8. Instala o CLI do Flutterfire:
    ```bash
    dart pub global activate flutterfire_cli
    ```

### 9. Instala o Firebase CLI:
    ```bash
    npm install -g firebase-tools
    ```

### 10. Verifica instalação do Firebase CLI, senão verificar PATH:
    ```bash
    firebase --version
    ```

### 11. Fazer login na sua conta do Firebase:
    ```bash
    firebase login
    ```

### 12. Executa o comando na raiz do projeto para configurar o Firebase no projeto
   (Observação: para mim, não funcionou no terminal do VSCode, somente no CMD):
    ```bash
    flutterfire configure
    ```

### 13. Após a configuração, será gerado um arquivo `firebase_options.dart` no mesmo diretório do `main.dart`.

### 14. Importar o `firebase_options.dart` no `main.dart`:
    ```dart
    import 'firebase_options.dart';
    ```

> **⚠️ IMPORTANTE:**  
> TALVEZ ESTEJA FALTANDO ALGO OU TENHA ALGO A MAIS QUE SEJA DESNECESSÁRIO.
