# Packet

This is cotunnel's packet library. Packet consist of opcode and data parts. You can write and read packets, send packets over your network implementation.

# How to use?

First of all, you need to import the library.

    import github.com/cotunnel/packet

Now, create our first packet.

    p := packet.Packet{}  
    p.New(1)  // this is opcode
    p.WriteByte(1)
    p.WriteInteger(1234)
    p.WriteString("this is test text")    

You can build packet with GetBytes() method. It includes packet length, opcode and data (we wrote byte, int, string).

    [0 24 0 1 1 0 0 4 210 0 17 116 104 105 115 32 105 115 32 116 101 115 116 32 116 101 120 116]

You can build packet object from using bytes with `Fill` method.

## Methods

 - WriteByte
 - WriteShort
 - WriteInteger
 - WriteString
 - WriteBytes
 - ReadByte
 - ReadShort
 - ReadInteger
 - ReadString
 - ReadBytes
 - Fill
 - GetBytes

## Author

   
 - [@araufdogan](https://github.com/araufdogan)
