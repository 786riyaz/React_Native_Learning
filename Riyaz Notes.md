npm install -g expo-cli

npx create-expo-app myMobileApp

cd myMobileApp
npm start


npm install @react-navigation/native
npm install react-native-screens react-native-safe-area-context
npm install @react-navigation/native-stack


import { View, Text } from "react-native";

export default function HomeScreen() {
  return (
    <View>
      <Text>Hello Mobile App</Text>
    </View>
  );
}