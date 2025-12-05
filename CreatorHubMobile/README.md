# Creator Hub Mobile

Versão mobile do Creator Hub desenvolvida com React Native e Expo.

## 🚀 Instalação e Execução

### Pré-requisitos
- Node.js 16+ 
- npm ou yarn
- Expo CLI
- Expo Go app no seu celular (para testes)

### Instalação

```bash
# Instalar dependências
npm install

# Instalar Expo CLI globalmente (se não tiver)
npm install -g @expo/cli
```

### Executar o projeto

```bash
# Iniciar o servidor de desenvolvimento
npx expo start

# Ou usar o comando npm
npm start

# Para Android
npx expo start --android

# Para iOS
npx expo start --ios

# Para web
npx expo start --web
```

## 📱 Como testar

1. Instale o app **Expo Go** no seu celular:
   - [Android - Google Play](https://play.google.com/store/apps/details?id=host.exp.exponent)
   - [iOS - App Store](https://apps.apple.com/app/expo-go/id982107779)

2. Execute `npx expo start`

3. Escaneie o QR code com:
   - **Android**: App Expo Go
   - **iOS**: Câmera nativa do iPhone

## 🏗️ Build para Produção

### Android (APK/AAB)

```bash
# Instalar EAS CLI
npm install -g @expo/eas-cli

# Login no Expo
eas login

# Configurar build
eas build:configure

# Build para Android
eas build --platform android

# Build para produção (Play Store)
eas build --platform android --profile production
```

### iOS (IPA)

```bash
# Build para iOS
eas build --platform ios

# Build para produção (App Store)
eas build --platform ios --profile production
```

## 📁 Estrutura do Projeto

```
CreatorHubMobile/
├── App.js                 # Componente principal
├── app.json              # Configurações do Expo
├── babel.config.js       # Configurações do Babel
├── package.json          # Dependências
├── assets/               # Imagens e ícones
│   ├── icon.png
│   ├── adaptive-icon.png
│   ├── splash.png
│   └── favicon.png
├── screens/              # Telas da aplicação
│   ├── LoginScreen.js
│   └── DashboardScreen.js
└── components/           # Componentes reutilizáveis
    └── PublishModal.js
```

## 🎨 Funcionalidades

- ✅ Tela de login com design responsivo
- ✅ Autenticação com Google, Apple e email/senha
- ✅ Dashboard com navegação por abas
- ✅ Busca de conteúdo
- ✅ Modal de publicação de conteúdo
- ✅ Lista horizontal de conteúdo em destaque
- ✅ Navegação entre telas
- ✅ Design otimizado para mobile
- ✅ Suporte a iOS e Android

## 🔧 Tecnologias

- **React Native** 0.72.10
- **Expo SDK** 49
- **React Navigation** 6
- **Expo Linear Gradient**
- **Expo Vector Icons**

## 📦 Publicação na Play Store

1. **Gerar build de produção:**
```bash
eas build --platform android --profile production
```

2. **Baixar o arquivo AAB gerado**

3. **Fazer upload na Google Play Console:**
   - Acesse [Google Play Console](https://play.google.com/console)
   - Crie um novo app ou selecione existente
   - Vá em "Versões do app" > "Produção"
   - Faça upload do arquivo AAB
   - Preencha as informações necessárias
   - Envie para revisão

## 🍎 Publicação na App Store

1. **Gerar build de produção:**
```bash
eas build --platform ios --profile production
```

2. **Fazer upload via App Store Connect:**
   - O EAS automaticamente faz upload para o TestFlight
   - Acesse [App Store Connect](https://appstoreconnect.apple.com)
   - Configure as informações do app
   - Envie para revisão

## 🐛 Solução de Problemas

### Erro de assets não encontrados
- Certifique-se que a pasta `assets/` existe
- Verifique se todos os arquivos de imagem estão presentes

### Problemas de dependências
```bash
# Limpar cache e reinstalar
rm -rf node_modules
npm install
npx expo install --fix
```

### Problemas com Expo CLI
```bash
# Usar a versão local do Expo
npx expo start

# Ao invés de
expo start
```

## 📄 Licença

Este projeto é privado e proprietário.