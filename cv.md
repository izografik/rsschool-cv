# iOS Developer

## Igor Chizhikov

## Contacts:
* gmail: izografik@gmail.com
* phone: + 375(29)5658710
* discord: Igor_Chizhikov#3765


## About me:
I am 30 years old. I'm a translator by education (MSLU, language: German), but 12years I work as an artist. A year ago I decided to devote my free time to programming. It was my hobby, but now I decided to take it seriously. What do I want? I want to become a top-notch mobile developer. 

## About my skills:

###### Hard:
* Swift
* UIKit
* Layout & constraints in code
* Foundation
* Git
* CocoaPods

###### Soft:
* “Master degree” in building good relationships
* Self management
* “Product-oriented thinking”
* Resolving conflicts in the team

## Latest code examples:

class MusicPlayer {
    static let shared = MusicPlayer()
    var audioPlayer: AVAudioPlayer?

    func startBackgroundMusic() {
        if let bundle = Bundle.main.path(forResource: "backgroundMusic", ofType: "mp3") {
            let backgroundMusic = NSURL(fileURLWithPath: bundle)
            do {
                audioPlayer = try AVAudioPlayer(contentsOf:backgroundMusic as URL)
                guard let audioPlayer = audioPlayer else { return }
                audioPlayer.numberOfLoops = -1
                audioPlayer.prepareToPlay()
                audioPlayer.play()
            } catch {
                print(error)
            }
        }
    }
    
    func stopBackgroundMusic() {
        guard let audioPlayer = audioPlayer else { return }
        audioPlayer.stop()
    }
}


