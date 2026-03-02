# Estrutura Básica - React Native

```jsx
// 1. IMPORTAÇÕES
// Importa componentes do React Native  e código de terceiros.
import React, { useState } from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';

// 2. COMPONENTE
// Componente funcional principal
export default function MeuComponente() {

  // 3. DECLARAÇÕES
  // Aqui declaramos variáveis, estados e funções que serão utilizados no componente

  // ESTADO (STATE)
  // useState cria uma variável reativa (estado) que permite atualizar a interface quando seu valor é alterado
  const [contador, setContador] = useState(0);

  // 4. FUNÇÕES
  // Função responsável por incrementar o valor do contador
  const aumentar = () => setContador(contador + 1);

  // 5. RENDER (JSX)
  // JSX define a estrutura visual do componente e é responsável por renderizar os elementos na tela
  return (
    <View style={styles.container}>
      {/* Text exibe o valor do contador */}
      <Text style={styles.texto}>Contador: {contador}</Text>

      {/* Button cria um botão clicável que executa a função aumentar */}
      <Button title="Aumentar" onPress={aumentar} />
    </View>
  );
}

// 6. ESTILOS
// StyleSheet é utilizado para definir e organizar estilos de forma performática
const styles = StyleSheet.create({
  container: {
    flex: 1,                 // Faz o container ocupar toda a tela
    justifyContent: 'center',// Centraliza os elementos verticalmente
    alignItems: 'center'     // Centraliza os elementos horizontalmente
  },
  texto: {
    fontSize: 20,            // Define o tamanho da fonte do texto
    marginBottom: 10         // Espaço abaixo do texto para separar dos botões
  }
});
```

---

## Explicação Formal e Detalhada de Cada Elemento

| Elemento      | Descrição Detalhada |
|---------------|-------------------|
| `View`        | Um **container** utilizado para estruturar a interface. Ele serve para agrupar outros componentes, definir layouts e aplicar estilos. Funciona de forma análoga a `<div>` no React para web. |
| `Text`        | Componente destinado a **exibir conteúdo textual** na tela. Todo texto no React Native deve ser encapsulado dentro de `Text` para ser renderizado corretamente. Permite aplicar estilos específicos para tipografia, como tamanho, cor e alinhamento. |
| `Button`      | Componente que cria um **botão nativo** da plataforma (Android ou iOS). Possui propriedades para título e ação (`onPress`), sendo utilizado para interações do usuário de forma simples. Para customizações visuais avançadas, pode-se utilizar `TouchableOpacity` ou `Pressable`. |
| `useState`    | Hook do React que cria um **estado interno** do componente. Permite armazenar valores que podem mudar ao longo do tempo, acionando uma atualização automática da interface quando alterados. Fundamental para criar interfaces dinâmicas e interativas. |
| Função (`aumentar`) | Função declarada dentro do componente para **modificar o estado**. Neste exemplo, incrementa o valor do contador. As funções dentro do escopo do componente podem acessar e atualizar os estados e props declarados. |
| JSX / return  | Representa o **código declarativo que define a interface**. É responsável por organizar os elementos visuais, componentes filhos e aplicar estilos. JSX é convertido em chamadas nativas pelo React Native para renderização na plataforma móvel. |
| `StyleSheet`  | Ferramenta utilizada para **definir e organizar estilos**. Permite aplicar propriedades visuais aos componentes de forma consistente, semelhante ao CSS, mas otimizado para desempenho em dispositivos móveis. Facilita a manutenção e padronização do layout da aplicação. |

---
