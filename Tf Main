//
//  ViewController.swift
//  Bord
//
//  Created by Adam Brook on 7/6/22.
//

import UIKit
import MessageUI

class ViewController: UIViewController, MFMailComposeViewControllerDelegate {
        
    
    @IBOutlet weak var outputLabel: UILabel!
    
    @IBOutlet weak var numberOutput: UILabel!
    
    
    
    
    let Activities = ["1. Go Mini Golfing!", "2. Watch a Movie!", "3. Read a Book!", "4. Clean your Room!", "5. Take a Walk!", "6. Draw!", "7. Cook something New!", "8. Learn a New Language!", "9. Pick Up Trash Around Your Neighboorhood!", "10. Write Down Your Goals!", "11. Meditate!", "12. Play a Board Game!", "13. Play a sport!", "14. Go on a Bike Ride!", "15. Listen to a New Music Playlist!", "16. Do a Crossword Puzzle!", "17. Create a Schedule for the Week!", "18. Call a Friend!", "19. Dance in your Room!", "20. Go Online Shopping!", "21. Google Yourself!", "22. Take a Nap!", "23. Flip a Water Bottle!", "24. Read a Magazine!","25. Look for Vacation Spots!", "26. Organize your Kitchen!", "27. Think of Summer Plans!", "28. Go to the Pool!", "29. Write a Song or Poem!", "30. Watch the Sunset!",  "31. Try a New Hairstyle!", "32. Take a Bath!", "33. Learn How to Juggle!", "34. Learn How to Whistle!", "35. Write a Letter to a Friend!", "36. Organize your Fridge!", "37. Make a Pillow Fort!", "38. Try on New Outfits!", "39. Make Paper Mache!", "40. Do a Handstand!", "41. Play a Card Game!", "42. Finish some Homework!", "43. Do 30 minutes of math!", "44. Build some legos!", "45. Go shoe shopping!", "46. Make a bath bomb!", "47. Start a blog!", "48. Make pottery!", "49. Take photos outside!", "50. Try to make origami!", "51. Color in a coloring book!", "52. Play some ping pong!", "53. Look at Colleges!", "54. Learn an Instrument!", "55. Make your Bed!", "56. Color something!", "57. Try Yoga!", "58. Do word search!", "59. Make a key locket!", "60. Organize your Calendar", "61. Go for a Hike!", "62. Fly a Kite!", "63. Start a Garden!", "64. Decorate Your Driveway!", "65. Go to a Farmers Market!" ]
    
    override func viewDidLoad() {
        super.viewDidLoad ()
        
        }
        // Do any additional setup after loading the view.
    
   
    
    @IBAction func buttonTouch(_ sender: Any) {
            let randomQuote = Int.random(in: 0...(Activities.count - 1))
            outputLabel.text = Activities[randomQuote]
        }
    
    
    
    @IBAction func taskNumberGen(_ sender: Any) {
        let taskNumberGen = Int.random(in: 1...65)
        numberOutput.text = String(taskNumberGen)
        
    }
    
    
    
    @IBAction func Contact(_ sender: Any) {
        if MFMailComposeViewController.canSendMail() {
            let contactComposer = MFMailComposeViewController()
            contactComposer.setSubject("TaskFast")
            contactComposer.setMessageBody("Add more Tasks", isHTML: false)
            contactComposer.setToRecipients(["TaskFast.inquires@gmail.com"])
            contactComposer.mailComposeDelegate = self
            self.present(contactComposer, animated: true, completion: nil)
            
            } else {
            print("Email Not Configured")
        }
        

}
    
    
    
    func mailComposeController(_ controller: MFMailComposeViewController, didFinishWith result: MFMailComposeResult, error: Error?) {
        
        switch result {
            
        case .cancelled:
            print("Mail is Cancelled")
            break
            
            
        case .saved:
            print("Mail is Saved")
            break

        case .sent:
            print("Mail is Sent")
            break
            
        case .failed:
            print("Mail Failed to Send")
            break
            
        default:
            break
            
        }
        controller.dismiss(animated: true)
                
        }
    
    
    @IBAction func privacyNav(_ sender: Any) {
        
        if let url = URL(string: "https://www.iubenda.com/privacy-policy/96054719") {
            
            UIApplication.shared.open(url)

        }
    }
    
    
    @IBAction func developerNav(_ sender: Any) {
   
        if let devT = URL(string: "https://twitter.com/adamb1738") {
            
            UIApplication.shared.open(devT)

            
        }
    
    }
    
    
}
            

        
