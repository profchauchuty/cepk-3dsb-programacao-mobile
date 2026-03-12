```jsx
// Importações
import { useState } from 'react'
import { View, Text, Button, StyleSheet} from 'react-native'

// Componente Principal
export default function App(){
    // Declarações
    const [contador, setContador] = useState(0)

    function aumentar(){
      setContador(contador + 1)
    }

    function diminuir(){
      // Código
    }

    return (
      <View style={styles.container}>
        <Text>Contador: {contador}</Text>
        <Button title="Aumentar" onPress={aumentar}/>
      </View>
    )
}

// Estilização
const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    padding: 10,
    borderWidth: 5,
    borderColor: 'red'
  },
  titulo: {

  },
  contador: {

  }
})
