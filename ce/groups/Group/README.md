#  Example
An example ce client that set group value. 

# Registry Key Definitions
Key: HKEY_LOCAL_MACHINE

Path: "Software\ElemezIntegration"

Value: "Group"

Type: String

## Group Changed
In order to raise a group changed event to the ce elemez client you must change a registry value on the device. 

# Example Code
``` c#
 string group = groupTextBox.Text;
 using (RegistryKey subKey = Registry.LocalMachine.CreateSubKey(@"Software\ElemezIntegration\"))
 {
  subKey.SetValue("Group", group, RegistryValueKind.String);
 }
```        
