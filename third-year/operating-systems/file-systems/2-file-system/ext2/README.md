# EXT2

BOOT - BLOCK GROUP 0 - BLOCK GROUP 1 ... BLOCK GROUP n

## Block groups
SUPER BLOCK (1) - GROUP DESCRIPTOR (N) - DATA BITMAP (1) - INODE BITMAP (1) - INODE TABLE (N) - DATA (N)


## Root dir
- BG = (inode - 1) / inodes_per_group
- index = (inode - 1) % inodes_per_group

## Dir
- Inode (4)
- Size (2)
- Name Length (1)
- Type (1)
- Name (count)


### Dir entries:
1. Entry 01
    - Inode: 0x02
    - Size: 0x000C = 12 bytes
    - Length: 0x02 = 2 bytes
    - Type: 0x02 = dir
    - Name: 0x2e2e = ..
2. Entry 02
    - Inode: 0x000b = 11
    - Size: 0x0014 = 20 bytes
    - Lenght: 0A = 10 bytes
    - Type: 0x02 = dir
    - Name: lost+found
3. Entry 03
    - Inode: 0x1401
    - Size: 0x0028
    - Length: 5
    - Type: 2 (dir)
    - Name: teste
4. Entry 04
    - Inode: 0x0D = 13
    - Size: 1964
    - Lenght: 9
    - Type: 1 (fil)
    - Name: teste.txt
