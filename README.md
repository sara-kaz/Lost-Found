# Lost and Found System

This JavaFX application helps manage lost and found items in a campus environment. It allows users to add, view, filter, and export records of lost and found items. The application uses JavaFX for the GUI and stores data in memory during runtime.

## Features
- Add new lost and found items
- View and filter items by location
- Export data to a CSV file
- Undo the deletion of records
- Visualize data using a pie chart
- Display current date and time

## Getting Started

### Prerequisites
- Java Development Kit (JDK) 8 or higher
- JavaFX SDK

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/lost-and-found-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd lost-and-found-system
   ```
3. Open the project in your preferred Java IDE (e.g., IntelliJ IDEA, Eclipse).

### Usage
1. Run the `Main.java` file to start the application.
2. Use the GUI to add, view, filter, delete, and export lost and found items.

## Files

### Source Files
- `Item.java`: Defines the Item class used for lost and found records.
- `LostFoundController.java`: The controller class handling the logic and interaction for the GUI.
- `Main.java`: The main entry point of the application.
- `Lost&Found.fxml`: FXML file for the GUI layout.
- `application.css`: CSS file for styling the application.

### Resources
- `logo.png`: Logo image used in the application.

### Example Code
#### LostFoundController.java
```java
package application;

import javafx.fxml.FXML;
import javafx.fxml.Initializable;
import javafx.scene.chart.PieChart;
import javafx.scene.control.*;
import javafx.scene.control.cell.PropertyValueFactory;
import javafx.collections.FXCollections;
import javafx.collections.ObservableList;
import javafx.collections.transformation.FilteredList;
import javafx.event.ActionEvent;
import javafx.animation.KeyFrame;
import javafx.animation.Timeline;
import javafx.util.Duration;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;
import java.io.PrintWriter;
import java.net.URL;
import java.time.LocalDate;
import java.util.*;

public class LostFoundController implements Initializable {
    @FXML
    private Button add, export, undo, delete;
    @FXML
    private ComboBox<String> status, Location;
    @FXML
    private DatePicker date;
    @FXML
    private TextField item, ID;
    @FXML
    private TextArea descrp, descArea;
    @FXML
    private TableView<Item> tableView;
    @FXML
    private TableColumn<Item, String> locationCol, itemCol, statusCol, IDCol, descpCol;
    @FXML
    private TableColumn<Item, LocalDate> dateCol;
    @FXML
    private PieChart chart;
    @FXML
    private ListView<String> listView;
    @FXML
    private Label currentDate, message;

    private ObservableList<Item> data = FXCollections.observableArrayList();
    private ObservableList<Item> backup = FXCollections.observableArrayList();
    private ObservableList<PieChart.Data> pieChartData = FXCollections.observableArrayList();
    private int[] buildingCounts = new int[9];
    private String[] statusList = { "Lost", "Found" };
    private String[] locations = { "Building A", "Building B", "Building C", "Building D", "GYM", "Auditorium", "Library", "Student Commons", "Welcome Center" };
    private String[] list = { "Building A", "Building B", "Building C", "Building D", "GYM", "Auditorium", "Library", "Student Commons", "Welcome Center", "All Locations" };
    private String[] pieColors = { "LIGHTCORAL", "BLUE", "SKYBLUE", "DARKRED", "DARKSLATEBLUE", "RED", "MAROON", "TEAL", "NAVY" };

    @FXML
    public void addButton(ActionEvent event) {
        // Implementation for adding a new record
    }

    @FXML
    public void exportButton(ActionEvent event) throws IOException {
        // Implementation for exporting data to CSV
    }

    @FXML
    public void deleteButton(ActionEvent event) {
        // Implementation for deleting a record
    }

    @FXML
    public void undoButton(ActionEvent event) {
        // Implementation for undoing a deletion
    }

    @Override
    public void initialize(URL arg0, ResourceBundle arg1) {
        // Initialization logic
    }
}
```
## Contact

For any questions or issues, please contact sarakhaled.kaz@gmail.com.

---
Feel free to reach out with any questions or feedback regarding this Lost and Found implementation in Java. Happy coding!
