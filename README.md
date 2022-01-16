### Hey there <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">

<a href="https://asilarslan.medium.com/">
  <img align="left" alt="Asil's Medium" width="22px" src="https://cdns.iconmonstr.com/wp-content/assets/preview/2018/240/iconmonstr-medium-2.png" />
</a>
<a href="https://www.linkedin.com/in/asilarslan/">
  <img align="left" alt="Asil's LinkedIN" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/linkedin.svg" />
</a>
<a href="https://github.com/asilarslan">
  <img align="left" alt="Asil's Counter" src="https://visitor-badge.glitch.me/badge?page_id=asilarslan.asilarslan" />
</a>

<br>
<br>

```swift

import Foundation

struct Profile: CustomStringConvertible {
    
    let name = "Asil Arslan"
    
    var description: String {
        """
        \(name)\n
        I am a software engineer focused on iOS development.
        Working on teams with project managers, developers, 
        and designers, I have built mobile applications and 
        SDKs focused on excellent user experience and design.
        I am looking to work in a collaborative environment 
        where I can develop products that improve people's lives.\n
        """
    }
    
    enum Skill: String, CaseIterable {
        case swift, objc, uIKit, swiftUI
        case testing, git, fastlane
        case vim, rN, combine
    }
    
    func proficient(in skills: [Skill] = Skill.allCases) -> String {
        skills
            .map(\.rawValue)
            .map(\.capitalized)
            .map { "- " + $0 + "\n" }
            .reduce("Skills: \n", +)
    }
}

// Paste into a playground!
let profile = Profile()
print(profile.description)
print(profile.proficient())

```
