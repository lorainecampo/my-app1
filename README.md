import React from 'react';
import Constants from 'expo-constants';
import { StyleSheet, Button, View, SafeAreaView, Text, Alert, Image, TextInput } from 'react-native';



const App = () => { 



const handleInicioPress = () => {
  Alert.alert('¡Menú!', 'bienvenido, comentar, informacion, salir.');
};

  const handleSalirPress = () => {
    Alert.alert(
      'Salir',
      '¿Estás seguro de que deseas salir?',
      [
        {
          text: 'Cancelar',
          style: 'cancel',
        },
        {
          text: 'Salir',
          onPress: () => {
            Alert.alert('¡Adiós!', 'Has salido de la aplicación.');
          },
        },
      ],
      { cancelable: false }
    );
  };

const Separator = () => <View style={styles.separator} />;

  return (
    <SafeAreaView style={styles.container}>
     
      <View style={styles.imageContainer}>

      <Button
        title="Inicio"
        onPress={handleInicioPress}
        color="#66CDAA"
        style={styles.button}
        

        />
        
        <Image source={{ uri: 'https://static.vecteezy.com/system/resources/previews/006/697/631/non_2x/business-analysing-seo-web-development-software-coding-and-programming-on-laptop-computer-with-graph-charts-script-language-testing-and-graphical-icons-vector.jpg' }}
         style={styles.image} />

      </View>
      
      <View>
        
        <Text style={styles.title}>
        Evidencia GA8-220501096-AA2-EV02 Desarrollar módulos versión móvil según requerimientos del proyecto con React Native 
        </Text>

        

        <Button
          title="Bienvenido"
          color="#C71585"
          onPress={() => Alert.alert('Hola, esta es la  evidencia presentada por loraine campo')}
        />

        
        <Separator />
      
        <View>    
          <Text style={styles.title}>
            Deja un comentario
          </Text>
          <TextInput style={styles.textInput} />
          
        </View>
        
        <Separator />
        
        <View style={styles.fixToText}>

          
          <Button
            title="guardar"
            color="#F4A460"
            onPress={() => Alert.alert('has hecho un comentario')}
          />
          
        </View>
        
        <Separator />
        
        <View>
          <Text style={styles.title}>
            Importante
          </Text>
          <Button
            title="informate"
            color="#66CDAA"
            onPress={() => Alert.alert('muy pronto ampliaremos nuestro menu, para una mejor experiencia')} 
          />
  
          <Separator />
          <Button
        title="Salir"
        onPress={handleSalirPress}
        color="#C71585"
        style={styles.button}
          />
  
        </View>
        
      </View>
    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    alignItems: 'center',
    marginTop: Constants.statusBarHeight,
    // justifyContent: 'center',
    marginHorizontal: 8,

 

  },
  image: {
    justifyContent: 'center',
    resizeMode: 'contain',
    height: 100
  
    
  },
  imageContainer: {
    marginTop: 80
    
  },
  textInput:{
    borderColor: '#F4A460',
    borderWidth: 1,
    height: 40
  },
  title: {
    textAlign: 'center',
    marginVertical: 8,
  },
  fixToText: {
    flexDirection: 'row',
    justifyContent: 'space-between',
  },
  separator: {
    marginVertical: 8,
    borderBottomColor: '#737373',
    borderBottomWidth: StyleSheet.hairlineWidth,
  }
});

export default App;

