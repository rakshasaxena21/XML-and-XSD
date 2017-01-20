# XML-and-XSD
MPT1
<?xml version="1.0"?>

<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="Electricity">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="Consumer" maxOccurs="100">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="Consumer_Name">
                <xs:simpleType>
                  <xs:restriction base="xs:string">
                    <xs:pattern value="[A-Z][a-z]+" ></xs:pattern>
                  </xs:restriction>
                </xs:simpleType>
              </xs:element>
              
              <xs:element name="Number_of_units">
                <xs:simpleType>
                  <xs:restriction base="xs:int">
                    <xs:pattern value="[0-9]*" ></xs:pattern>
                  </xs:restriction>
                </xs:simpleType>
              </xs:element>
            
              <xs:element name="email" type="xs:string"></xs:element>
          

            </xs:sequence>
            <xs:attribute name="Consumer_Number" type="xs:integer" use="required"></xs:attribute>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>




  ------ .XML FILE

  <?xml version="1.0"?>
<Electricity xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="electricity.xsd">
  <Consumer Consumer_Number="123">
    <Consumer_Name>Rohan</Consumer_Name>
  <Number_of_units>100</Number_of_units>
    <email>rohan@electricty.com</email>
  </Consumer>

  </Electricity>
