# TabbarApp_Swift_storyboard
Creating a tab bar application using Swift with Storyboard and Interface Builder involves several steps. Below is a comprehensive guide to help you set it up in Xcode.

### Steps to Create a Tab Bar Application

1. **Create a New Xcode Project**:
   - Open Xcode and select **Create a new Xcode project**.
   - Choose **App** under the iOS section and click **Next**.
   - Enter your project name (e.g., `TabBarApp`) and make sure to select **Storyboard** for the Interface. Choose Swift as the language and click **Next**.
   - Choose a location to save your project and click **Create**.

2. **Set Up the Main Interface**:
   - Open `Main.storyboard`. You’ll see a blank view controller.

3. **Add a Tab Bar Controller**:
   - In the Object Library (the right pane), search for **Tab Bar Controller**.
   - Drag the **Tab Bar Controller** into your storyboard. This automatically adds two view controllers connected to the tab bar.

4. **Add View Controllers**:
   - Select one of the default view controllers (the ones that are connected to the tab bar).
   - In the Object Library, find and drag a **UIViewController** for each additional tab you want (e.g., Home, Settings).
   - You can drag as many view controllers as you need.

5. **Set Up Segues**:
   - Control-drag from the **Tab Bar Controller** to each of the view controllers you added to create segues. Choose **view controllers** for the segue type.

6. **Configure Tab Bar Items**:
   - Select each view controller you created (one at a time).
   - In the Attributes Inspector (right pane), you can set the **Title** and **Image** for the tab bar item.
   - For example:
     - **Home**: Title = "Home", Image = "house" (select a system image or add your own).
     - **Settings**: Title = "Settings", Image = "gear".

7. **Create Custom View Controller Classes**:
   - For each view controller, create a corresponding Swift class. Right-click on your project folder and select **New File** -> **Swift File**. Name it (e.g., `HomeViewController.swift`, `SettingsViewController.swift`).
   - Make sure to set the class of each view controller in the storyboard:
     - Select a view controller in the storyboard, and in the Identity Inspector (right pane), set the **Class** to your custom class (e.g., `HomeViewController`).

### Example Code for Custom View Controllers

Here’s a simple example of what the custom view controllers might look like.

**HomeViewController.swift**:
```swift
import UIKit

class HomeViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        view.backgroundColor = .white
        
        // Add a label to the home view
        let label = UILabel()
        label.text = "Home View"
        label.font = UIFont.systemFont(ofSize: 24)
        label.textAlignment = .center
        label.translatesAutoresizingMaskIntoConstraints = false
        view.addSubview(label)
        
        // Constraints for the label
        NSLayoutConstraint.activate([
            label.centerXAnchor.constraint(equalTo: view.centerXAnchor),
            label.centerYAnchor.constraint(equalTo: view.centerYAnchor)
        ])
    }
}
```

**SettingsViewController.swift**:
```swift
import UIKit

class SettingsViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        view.backgroundColor = .lightGray
        
        // Add a label to the settings view
        let label = UILabel()
        label.text = "Settings View"
        label.font = UIFont.systemFont(ofSize: 24)
        label.textAlignment = .center
        label.translatesAutoresizingMaskIntoConstraints = false
        view.addSubview(label)
        
        // Constraints for the label
        NSLayoutConstraint.activate([
            label.centerXAnchor.constraint(equalTo: view.centerXAnchor),
            label.centerYAnchor.constraint(equalTo: view.centerYAnchor)
        ])
    }
}
```

### Final Steps

1. **Set Initial View Controller**:
   - Select the Tab Bar Controller in the storyboard.
   - Go to the **Attributes Inspector** and check the box for **Is Initial View Controller**.

2. **Run the App**:
   - Select a simulator or a physical device.
   - Click the **Run** button (▶️) in Xcode to build and run your app.

### Complete Project Structure
- Your project will have the following structure:
  ```
  TabBarApp
  ├── TabBarApp.xcodeproj
  ├── AppDelegate.swift
  ├── SceneDelegate.swift
  ├── HomeViewController.swift
  ├── SettingsViewController.swift
  └── Main.storyboard
  ```

### Conclusion
You now have a simple tab bar application with two tabs (Home and Settings) using Storyboard and Interface Builder. You can further customize the view controllers, add more tabs, or implement additional features as needed.

If you have any questions or need further assistance, feel free to ask! 😊
