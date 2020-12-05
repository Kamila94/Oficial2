import React, { useState } from 'react';
import { Button, Text, View, StyleSheet } from 'react-native';

export default function App() {
  // contador e uma variavel no estado da aplicacao e setContador permite alterar esse valor.
  // os dois foram criados com useState.
  const [contador, setContador] = useState(0);

  return (
    <View style={styles.container}>
      <Text style={styles.label}>Clique aqui</Text>
      <Button title={'' - contador} onPress={() => setContador(contador - 1)} />
      <Button title={'' + contador} onPress={() => setContador(contador + 1)} />
      <Button title={'Reset'} color="#8f8359" onPress={() => setContador(0)} />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    backgroundColor: '#ecf0f1',
    padding: 8,
  },
  label: {
    textAlign: 'center',
    padding: 5,
  },
});
