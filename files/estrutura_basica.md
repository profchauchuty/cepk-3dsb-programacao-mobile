# Estrutura Básica - React Native

```jsx
// Importações:
// Importa componentes do React Native e bibliotecas de terceiros necessárias para a aplicação
import React, { useState } from 'react';
import { StyleSheet, Text, View, Button } from 'react-native';

// Componente Principal:
// Componente funcional principal que representa a tela ou parte da aplicação
export default function App() {

  // Declarações de variáveis/estados e funções
  // Onde declaramos estados, constantes e funções que controlam o comportamento do componente
  const [contador, setContador] = useState(0); // Estado que armazena o valor do contador

  const aumentar = () => setContador(contador + 1); // Função que incrementa o contador

  // Renderização:
  // JSX define o que será exibido na tela
  return (
    <View style={styles.container}>
      <Text>
        Contador: {contador}
      </Text>
      <Button title="Aumentar" onPress={aumentar} />
    </View>
  );
}

// Estilização:
// StyleSheet organiza os estilos aplicados aos componentes
const styles = StyleSheet.create({
  container: {
    flex: 1,                 // Faz o container ocupar toda a tela
    justifyContent: 'center',// Centraliza verticalmente
    alignItems: 'center'     // Centraliza horizontalmente
  }
});
```
