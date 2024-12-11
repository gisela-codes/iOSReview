# iOS Review
## Jump To:
- [View Controller](#vc)
- [Table View Delegates](#tb)
## 1. Format Layout in Main
<img src="main.png" width="400">

**Nav Controller should be set as 'Is Inital View Controller'*

## <a name="vc"></a>2. Create ViewController Classes

### a. Define classes
```swift
import UIKit

class AffirmationViewController: UIViewController {
    
}
```
```swift
import UIKit

class ItemCell: UITableViewCell {
    
    @IBOutlet var DateLabel: UILabel!
    @IBOutlet var SentenceLabel: UILabel!
}

```
## b. Add custom class to storyboard VC's (View Controllers)
<img src="class.png" width="300">

*Repeat with TableView Cell VC**

## c. Connect to outlets
<img src="connections.png">

## <a name="tb"></a>TableView Delegates
For my data, I will start small by having 3 records
```swift
//a list of tuples
var affirmations: [(date: String, text: String)] = [
        ("12/4", "I will pass this final"),
        ("12/5", "I am capable of great things"),
        ("12/6", "Every day I grow stronger")
    ]
```
### numberOfRowsInSection
//  the amount of rows
```swift 
//  the amount of rows (3 in this case)
override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return affirmations.count
    }
```
### cellForRowAt
```swift
override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    // tb view cell has the identifier 'AffirmationCell', type cast it as a cell
    let cell = tableView.dequeueReusableCell(withIdentifier: 
    "AffirmationCell", for: indexPath) as! AffirmationCell

    let affirmation = affirmations[indexPath.row]

    cell.DateLabel.text = affirmation.date
    cell.SentenceLabel.text = affirmation.text
    return cell
    }
```