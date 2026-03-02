# Componentes Fundamentais do React Native

O **React Native** é um framework mantido pela Meta que possibilita o desenvolvimento de aplicações móveis nativas para Android e iOS utilizando JavaScript e os princípios da biblioteca React. Seu principal diferencial é permitir alto reaproveitamento de código entre plataformas, mantendo desempenho próximo ao nativo.

Este documento apresenta, de forma estruturada e formal, os principais componentes utilizados no desenvolvimento com React Native.

---

# 1. Componentes Estruturais

## 1.1 View

O componente `View` é a base da estrutura visual no React Native. Ele é utilizado como contêiner para organizar e agrupar outros componentes.

Pode ser comparado a:

- `<div>` no React para Web  
- `ViewGroup` no Android  
- `UIView` no iOS  

### Exemplo:

```jsx
import { View } from 'react-native';

export default function App() {
  return (
    <View>
      {/* Conteúdo da aplicação */}
    </View>
  );
}
```

### Finalidades principais:

- Estruturação de layout  
- Agrupamento de elementos  
- Aplicação de estilos e organização via Flexbox  

---

## 1.2 Text

O componente `Text` é responsável pela renderização de textos na interface.

Diferentemente do ambiente web, no React Native todo conteúdo textual deve obrigatoriamente estar encapsulado dentro de um componente `Text`.

### Exemplo:

```jsx
import { Text } from 'react-native';

<Text>Olá, mundo!</Text>
```

---

## 1.3 Image

O componente `Image` é utilizado para exibir imagens locais ou remotas.

É obrigatório definir explicitamente as dimensões da imagem (largura e altura).

### Exemplo:

```jsx
import { Image } from 'react-native';

<Image
  source={{ uri: 'https://exemplo.com/imagem.png' }}
  style={{ width: 120, height: 120 }}
/>
```

---

# 2. Componentes de Exibição de Listas e Rolagem

## 2.1 ScrollView

O componente `ScrollView` permite que o conteúdo ultrapasse os limites da tela, habilitando rolagem vertical ou horizontal.

### Exemplo:

```jsx
import { ScrollView, Text } from 'react-native';

<ScrollView>
  <Text>Conteúdo extenso...</Text>
</ScrollView>
```

### Indicações de uso:

- Telas com quantidade moderada de conteúdo  
- Conteúdo predominantemente estático  

Para grandes volumes de dados, recomenda-se a utilização do `FlatList`.

---

## 2.2 FlatList

O componente `FlatList` é otimizado para renderização de listas extensas. Ele realiza renderização sob demanda, garantindo melhor desempenho e uso eficiente de memória.

### Exemplo:

```jsx
import { FlatList, Text } from 'react-native';

const dados = [
  { id: '1', nome: 'João' },
  { id: '2', nome: 'Maria' }
];

export default function Lista() {
  return (
    <FlatList
      data={dados}
      keyExtractor={(item) => item.id}
      renderItem={({ item }) => <Text>{item.nome}</Text>}
    />
  );
}
```

### Principais vantagens:

- Alta performance  
- Renderização incremental  
- Melhor gerenciamento de memória  

---

# 3. Componentes de Interação

## 3.1 Button

O componente `Button` representa um botão nativo básico.

### Exemplo:

```jsx
import { Button } from 'react-native';

<Button
  title="Confirmar"
  onPress={() => alert('Ação executada')}
 />
```

Observação: sua capacidade de personalização visual é limitada. Para maior controle, recomenda-se o uso de `TouchableOpacity` ou `Pressable`.

---

## 3.2 TouchableOpacity

O componente `TouchableOpacity` permite criar áreas interativas com efeito visual de opacidade ao serem pressionadas.

### Exemplo:

```jsx
import { TouchableOpacity, Text } from 'react-native';

<TouchableOpacity onPress={() => console.log('Pressionado')}>
  <Text>Clique aqui</Text>
</TouchableOpacity>
```

É amplamente utilizado para:

- Botões personalizados  
- Cartões interativos  
- Elementos clicáveis com design customizado  

---

## 3.3 TextInput

O componente `TextInput` é utilizado para capturar dados digitados pelo usuário.

### Exemplo:

```jsx
import { TextInput } from 'react-native';

<TextInput
  placeholder="Digite seu nome"
  style={{ borderWidth: 1, padding: 10 }}
/>
```

Aplicações comuns:

- Formulários  
- Autenticação (login)  
- Cadastros  

---

# 4. Estilização

## 4.1 StyleSheet

O módulo `StyleSheet` permite organizar e estruturar estilos de forma eficiente e performática.

O React Native utiliza Flexbox como padrão para organização de layout.

### Exemplo:

```jsx
import { StyleSheet } from 'react-native';

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center'
  }
});
```

Vantagens:

- Organização do código  
- Melhor legibilidade  
- Padronização visual  
- Otimização interna de desempenho  

---

# 5. Conceitos Fundamentais

## 5.1 Props

As *props* (properties) permitem a passagem de dados entre componentes.

### Exemplo:

```jsx
import { Text } from 'react-native';

function Saudacao({ nome }) {
  return <Text>Olá, {nome}!</Text>;
}
```

As props tornam os componentes reutilizáveis e dinâmicos.

---

## 5.2 State

O *state* representa dados internos e dinâmicos de um componente. Quando o state é alterado, o componente é re-renderizado.

### Exemplo:

```jsx
import { useState } from 'react';
import { View, Text, Button } from 'react-native';

export default function Contador() {
  const [valor, setValor] = useState(0);

  return (
    <View>
      <Text>Valor atual: {valor}</Text>
      <Button
        title="Incrementar"
        onPress={() => setValor(valor + 1)}
      />
    </View>
  );
}
```

---

# 6. Síntese dos Componentes

| Componente        | Finalidade Principal                     |
|-------------------|------------------------------------------|
| View              | Estrutura e agrupamento de layout        |
| Text              | Exibição de conteúdo textual             |
| Image             | Exibição de imagens                      |
| ScrollView        | Rolagem de conteúdo                      |
| FlatList          | Renderização otimizada de listas         |
| Button            | Botão nativo básico                      |
| TouchableOpacity  | Área interativa personalizável           |
| TextInput         | Entrada de dados do usuário              |
| StyleSheet        | Organização e padronização de estilos    |

---

# Conclusão

O domínio desses componentes e conceitos constitui a base para o desenvolvimento de aplicações móveis em React Native. A correta utilização de estruturas de layout, componentes interativos, gerenciamento de estado e boas práticas de estilização permite a construção de interfaces robustas, escaláveis e alinhadas às diretrizes de desenvolvimento multiplataforma.
