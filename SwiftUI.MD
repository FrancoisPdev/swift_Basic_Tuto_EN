/* ************************************************************** *
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
 **************************************************************** */


# Start an basic hello world custom
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
/* ************************************************************** *
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
 **************************************************************** */


# Start a basic geometric in SwiftUI

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
/* ************************************************************** *
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
 **************************************************************** */

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
/* ************************************************************** *
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
                                                                   
 **************************************************************** */

# Start an basic Button with SwiftUI



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
/* ************************************************************** *
                                                                   
                                                                   
            Thank's for Watch'in web surfer                                             
                                                                   
                                                                   
                                                                   
 **************************************************************** */

