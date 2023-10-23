function extractContactInfo() {
  // Get the URL of the website.
  var url = "https://example.com/contact";

  // Get the Google Sheet.
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName("Sheet1");

  // Extract the contact information from the website.
  var firstName = sheet.getRange("A1").getValue();
  var lastName = sheet.getRange("B1").getValue();
  var email = sheet.getRange("C1").getValue();
  var phone = sheet.getRange("D1").getValue();
  var address = sheet.getRange("E1").getValue();

  // Populate the Google Sheet with the contact information.
  sheet.getRange("A2").setValue(firstName);
  sheet.getRange("B2").setValue(lastName);
  sheet.getRange("C2").setValue(email);
  sheet.getRange("D2").setValue(phone);
  sheet.getRange("E2").setValue(address);
}
