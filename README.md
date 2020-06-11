# Criando-controles-com-Xamarim-Forms
Exemplo de controle xamarim forms

Como criar controles xamarim forms (modificando o tutorial da Microsoft https://docs.microsoft.com/pt-br/xamarin/xamarin-forms/user-interface/layouts/contentview)


*a classe controle já está criada, você pode criar uma nova se quiser* 


1-	Na classe CONTROLE Estancia uma propriedade (eu quis colocar uma nova propriedade de cor de título para os cardview) 

public static readonly BindableProperty CardTitleProperty1 = BindableProperty.Create(nameof(CardTextColor), typeof(Color), typeof(CardView), Color.Default);


2-	Faça o código get e set para pegar os valores (do título)

        public Color CardTextColor 
        {
            get => (Color)GetValue(CardView.CardTitleProperty1);
            set => SetValue(CardView.CardTitleProperty1, value);
        }


3-	Coloque no xaml do controle o binding para referenciar 
              
              TextColor="{Binding CardTextColor}"


4-	Agora é só implementar e pronto, você pode está criando varias outras coisas, é tipo css do xamarim.

<controls:CardView BorderColor="Black"
                   CardColor="Yellow" 
                     CardTextColor="Red" //Este é o que criamos
                   CardTitle="Gustavo Batista Lima" 
                   CardDescription="texto"
                   IconBackgroundColor="SlateGray"
