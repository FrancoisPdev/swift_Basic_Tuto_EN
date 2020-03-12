[Start an basic Hello World custom](#start-an-basic-hello-world-custom)

[Start a basic geometric build in SwiftUI](#start-a-basic-geometric-build-in-swiftui)

[Start a basic profil with SwiftUI](#start-a-basic-profil-with-swiftui)

[Start an basic Button and ramdom-quote with SwiftUI](#start-an-basic-button-and-ramdom-quote-with-swiftui)

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

/* ************************************************************** *
                                                                   
                                                                   
            Thank's for Watch'in web surfer                                             
Useful source from Github [here](https://github.com/SimpleBoilerplates/SwiftUI-Cheat-Sheet#button)
                                                                   
                                                                   
 **************************************************************** */

