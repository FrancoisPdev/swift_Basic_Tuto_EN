[Start an basic Hello World custom](#start-an-basic-hello-world-custom)

[Start a basic geometric build in SwiftUI](#start-a-basic-geometric-build-in-swiftui)

[Start a basic profil with SwiftUI](#start-a-basic-profil-with-swiftui)

[Start an basic Button and ramdom-quote with SwiftUI](#start-an-basic-button-and-ramdom-quote-with-swiftui)

[Start a button background-color with SwiftUI](#start-a-button-background-color-with-swiftui)

[Start build an control flow temperature with SwiftUI](#start-build-an-control-flow-temperature-with-swiftui)

[Start build 3 custom buttons with compoment with SwiftUI](#start-build-3-custom-buttons-with-compoment-with-swiftui)

[Start simple Notifications view in SwiftUI](#start-simple-notifications-view-in-swiftui)

[Start simple Neumophisme Rectangle() in SwiftUI](#start-simple-neumorphisme-rectangle()-in-swiftui)

![Swift](https://miro.medium.com/max/2200/1*S4__g3knEbuuE6qHyWIbNQ.png)

# Start an basic Hello World custom

    //
    //  SwiftUIView.swift
    //  exo_Swift
    //
    //  Created by PARENT François on 12/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

    import SwiftUI

    struct SwiftUIView: View {
    
    var body: some View {
        
        VStack {
            Spacer()
            Text("Hello").font(.largeTitle).fontWeight(.ultraLight).foregroundColor(Color.orange).padding(1)
            Text("François").font(.largeTitle).fontWeight(.ultraLight).foregroundColor(Color.orange).multilineTextAlignment(.center).padding(50)
            
            Spacer()
        }
        
    }
}

    struct SwiftUIView_Previews: PreviewProvider {
        static var previews: some View {
            SwiftUIView()
        }
    }

***

# Start a basic geometric build in SwiftUI

    //
    //  SwiftUIView2.sfit.swift
    //  exo_Swift
    //
    //  Created by PARENT François on 12/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

import SwiftUI

struct SwiftUIView2_sfit: View {
    
    
    var body: some View {
        
        ZStack {
            
            Color.red
            
            Rectangle()
                .foregroundColor(Color.green)
                .frame(width: 200, height: 200)

            Circle()
                .foregroundColor(Color.blue)
                .frame(width: 100, height: 100)

            
            
                
            Text("Hello, World!")
                .font(.subheadline)
                .fontWeight(.ultraLight)
                .foregroundColor(Color.black)
            
        }
        
        }
    }

    struct SwiftUIView2_sfit_Previews: PreviewProvider {
        static var previews: some View {
            SwiftUIView2_sfit()
        }
    }

***

# Start a basic profil with SwiftUI


    //
    //  SwiftUIView3.swift
    //  exo_Swift
    //
    //  Created by PARENT François on 12/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

import SwiftUI

struct SwiftUIView3: View {
    var body: some View {
        VStack {

            HStack{
                Image(systemName: "person.circle")
                    .resizable()
                    .frame(width: 110, height: 110)
                    .foregroundColor(.orange)
                
            }
            
            VStack(alignment: .leading){
            Text("Danilo SANTANA")
                .bold()
                .font(.system(Font.TextStyle.largeTitle))
                
            Text("Brasil")
                .foregroundColor(.gray)
            }
                RoundedRectangle(cornerRadius: 50)
                    .padding(.horizontal)
                    .foregroundColor(.gray)
        }
            
    }
        

    }
    struct SwiftUIView3_Previews: PreviewProvider {
        static var previews: some View {
            SwiftUIView3()
        }
    }

***

# Start an basic Button and ramdom-quote with SwiftUI



        //
        //  SwiftUIViewButton.swift
        //  exo_Swift
        //
        //  Created by PARENT François on 12/03/2020.
        //  Copyright © 2020 PARENT François. All rights reserved.
        //

    import SwiftUI

    struct SwiftUIViewButton: View {


        @State var random = "c ki?"

        let quotes = [
        "Now is the time for all good men to come to the aid of their country",
        "Vini, vidi, vichi",
        "I regret that I have but one life to give for my country",
        "Illegitimi non carborundum"
        ]

        var body: some View {
            VStack{
                Text(random)
                .font(.subheadline)
                .foregroundColor(Color.green)
                .lineSpacing(10)
                .lineLimit(nil)
                .padding(60)
                Spacer().frame(height:40)
                Button("Who is there", action: {
                        self.random =
                            self.quotes.randomElement()!
                    }
                    ).padding(20).background(Color.blue).foregroundColor(Color.white).cornerRadius(20)
            }
        }


    }
    struct SwiftUIViewButton_Previews: PreviewProvider {
        static var previews: some View {
            SwiftUIViewButton()
        }
    }

***

# Start a button background-color with SwiftUI

    //
    //  BackgroundColorSwipe.swift
    //  exo_Swift
    //
    //  Created by PARENT François on 12/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

    import SwiftUI

    struct BackgroundColorSwipe: View {

        @State var swipe = Color.yellow

        var body: some View {
            ZStack{
                swipe.edgesIgnoringSafeArea(.all)
                Spacer()
                    .frame(height: 600)
                HStack{
                    Button("green",
                           action: {
                            self.swipe = Color.green

                    })
                        .padding(10)
                        .foregroundColor(Color.white)
                        .background(Color.green)
                        .cornerRadius(20)
                    Button("red",
                           action: {
                            self.swipe = Color.red

                    })
                        .padding(10)
                        .foregroundColor(Color.white)
                        .background(Color.red)
                        .cornerRadius(20)

                    Button("blue",
                           action: {
                            self.swipe = Color.blue

                    })
                        .padding(10)
                        .foregroundColor(Color.white)
                        .background(Color.blue)
                        .cornerRadius(20)
                }
            }
        }
    }

    struct BackgroundColorSwipe_Previews: PreviewProvider {
        static var previews: some View {
            BackgroundColorSwipe()
        }
    }

***

# Start build an control flow temperature with SwiftUI


    //
    //  Start_build_an_control_flow_temperature.swift
    //  exo_Swift
    //
    //  Created by PARENT François on 13/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

    import SwiftUI

    struct Start_build_an_control_flow_temperature: View {
        @State private var temperature: Double = 0.0
    
    var body: some View {
        ZStack{
            
    /*
    //            RadialGradient(gradient: Gradient(colors: [.white, .yellow]), center: .center, startRadius: 50, endRadius: 350)
    //                .edgesIgnoringSafeArea(.all)
    */

                if temperature > 20 {
                    Color.red.edgesIgnoringSafeArea(.all)
                }else {
                    Color.blue.edgesIgnoringSafeArea(.all)
                }

                VStack{

                if temperature >= 32 {

                    Text("Ne sortez pas !").foregroundColor(.black)

                    }
                else if temperature < -10 {
                    Text("Sortez et gelé !!")

                }else {
                    Text("il fait froid").foregroundColor(.black)
                }
                Text(" \(Int(temperature))°")
                    Slider(value: $temperature, in: -100...100, step: 1.0).padding(100).accentColor(.black)

                }

            }
        }
    }

    struct Start_build_an_control_flow_temperature_Previews: PreviewProvider {
        static var previews: some View {
            Start_build_an_control_flow_temperature)
        }
    }

***

# Start build 3 custom buttons with compoment with SwiftUI



    //
    //  trainningCompoment.swift
    //  exo_Swift
    //
    //  Created by PARENT François on 13/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //
    
    import SwiftUI
    
    struct trainningCompoment: View {
        
        var body: some View {
            
            ZStack{
                
                Color.yellow.edgesIgnoringSafeArea(.all)
                
                HStack{
                    customButtons(
                        customBackground: .red,
                        customForeGround: .white,
                        customImages: "play.rectangle.fill")
                    customButtons(
                        customBackground: .blue,
                        customForeGround: .white,
                        customImages: "paperplane")
                    customButtons(
                        customBackground: .green,
                        customForeGround: .white,
                        customImages: "smoke.fill"
                    )
                }
            }
        }
    }
    
    struct customButtons: View {
        
        var customBackground: Color
        var customForeGround: Color
        var customImages: String
        
        var body: some View {
            Button(action: {
                
            },
                   label: {
                    Image(systemName: "\(customImages)")
                        .padding(20)
                        .background(customBackground)
                        .foregroundColor(customForeGround)
                        .cornerRadius(12)
                    
            }
            )
        }
    }
    
    struct trainningCompoment_Previews: PreviewProvider {
        static var previews: some View {
            trainningCompoment()
        }
    }

***

# Start simple Notifications view in SwiftUI 

    //
    //  notification.swift
    //  App
    //
    //  Created by PARENT François on 17/03/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //
    // La page fonctionne avec de la données brute, nous avons simulés une fausse BDD pour ensuite recuperer les informations.
    // plus bas, "notification_Previews" permet de tester les elements sur l'Iphone.
    // remplacer destination:Text("hello") par la page que vous voulez
    // remplacer destination:Text("hello")2 par la page que vous voulez aussi

    import SwiftUI

    struct notification: View {
    
    
    var body: some View {
        
        VStack{
            List {
                ForEach(notifications){ notification in
                    NavigationLink(destination: Text("hello")){
                        Text(notification.invitation)
                        
                    }
                    NavigationLink(destination: Text("Yé soui sénorita75 é lé paquito komé toé yé lé zaime")){
                        Text(notification.request)
                        
                    }
                }
            }
        }.navigationBarTitle("Notifications")
    }
}

    // test de navigation pour l'ecran notification

    struct notification_Previews: PreviewProvider {
        static var previews: some View {
            NavigationView(){
                notification()
            }
        }
    }
***

# Start simple Neumophisme Rectangle() in SwiftUI

    //
    //  ContentView.swift
    //  Neumorphism
    //
    //  Created by PARENT François on 05/05/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

    import SwiftUI

    struct ContentView: View {

    var body: some View {
    
        ZStack {
            Color.offWhite
            RoundedRectangle(cornerRadius: 25)
            .fill(Color.offWhite)
            .frame(width: 300, height: 300)

        }.shadow(color: Color.black.opacity(0.2), radius: 10, x: 10, y: 10)
            .shadow(color: Color.white.opacity(0.7), radius: 10, x: -5, y: -5)
        .edgesIgnoringSafeArea(.all)
        
        
    }
    }

    struct ContentView_Previews: PreviewProvider {

    static var previews: some View {
    
        ContentView()
    }
    }

###### W/ this other file in the same folder

    //
    //FileNeumorphism.swift
    //  Neumorphism
    //
    //  Created by PARENT François on 05/05/2020.
    //  Copyright © 2020 PARENT François. All rights reserved.
    //

    import SwiftUI

    extension Color {
    static let offWhite = Color(red: 225 / 255, green: 225 / 255, blue: 235 / 255)
    }


/* ************************************************************** *
                                                                   
                                                                   
            Thank's for Watch'in web surfer                                             
Useful source from :
* Github [here](https://github.com/SimpleBoilerplates/SwiftUI-Cheat-Sheet#button)
* YouTube [here](https://www.youtube.com/playlist?list=PLuoeXyslFTuZRi4q4VT6lZKxYbr7so1Mr)
* PlayGround for browser [here](https://swiftui-playground.kishikawakatsumi.com)                                                                   
                                                                   
 **************************************************************** */

