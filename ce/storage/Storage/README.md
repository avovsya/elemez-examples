#  Example
An example ce client that set storage value. 

# Registry Key Definitions
Key: HKEY_LOCAL_MACHINE

Path: "Software\ElemezIntegration"

Value: "EFWN"

Type: DWord

## Wear Level Changed
In order to raise a wear level changed event to the ce elemez client you must change a registry value on the device. 

# Example Code
``` c#
 var flashWearCycles = uint.Parse(flashWearCyclesTextBox.Text);
 using (var subKey = Registry.LocalMachine.CreateSubKey(@"Software\ElemezIntegration\"))
 {
   subKey.SetValue("EFWN", flashWearCycles, RegistryValueKind.DWord);
 }
```        
