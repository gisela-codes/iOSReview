# Review For Final
## TableView/Nav
### Table View Controller
``` swift
import UIKit

class VeggiesViewController: UITableViewController {
    override func viewDidLoad(){
        super.viewDidLoad()
    }
    override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return 5; // Returns 5 rows in my tableview
    }
    override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = table
        return 5; // Returns 5 rows in my tableview
    }

}

```
Create the class
create the view
create the identifier
typecast correctly
### Prepare for segue
1. Click the segure and give it an identifier
```swift
    override func preper(for segure: UIStoryboardSegure, sender: Any?){
        if segure.identifier == "showDetails"{
            // get the destination controller
            let desitination = sefure.destination as! DetailsViewController
            // typecase to correct controller class
            // identifiy the data to send
            if let indexPath =
            //assign some property on destination vc

        }
    }
```
**Click on is initial view controller**
## UI/ Organization
## API
### How to print url
``` swift
if let jsonData = data{
    if let jsonString = String(data: jsonData, encoding: .utf8)
}
```
## Other