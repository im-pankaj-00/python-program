import json

import requests

pincode = input("pincode ")
type(pincode)

pincode_info = requests.get('http://postalpincode.in/api/pincode/' + pincode)
if pincode_info.status_code == 200:
    pincodedetails = json.loads(pincode_info.content.decode('utf-8'))
    print('District is: ' + pincodedetails['PostOffice'][0]['District'])
    print('State is: ' + pincodedetails['PostOffice'][0]['State'])
    print('Country is: ' + pincodedetails['PostOffice'][0]['Country'])
else:
    print('[!] Request Failed')
