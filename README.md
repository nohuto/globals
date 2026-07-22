# Globals

Global = data object stored at a fixed location. This was created using IDA by combining matching PDB symbols & types with PE metadata.

Used for the [diff](https://noverse.dev/diff) section, each file can include a symbol name, RVA, PE section, type, storage size, initial value (decimal as comment). Note that the init value doesn't always equal to the current value, as for example the PE has `KeMaximumIncrement` of `0`, and during the kernel init it gets changed.

```cpp
// RVA 0xD1EA54, ALMOSTRO
int KeMaximumIncrement = 0x00000000; // 0

lkd> dd KeMaximumIncrement L1
fffff805`4591ea54  0002625a
```

## Versions & Build Reference

| Version | Name | Build number |
|---|---|---|
| `1507` | Windows 10 1507 | `10240` |
| `1511` | Windows 10 1511 | `10586` |
| `1607` | Windows 10 1607 | `14393` |
| `1703` | Windows 10 1703 | `15063` |
| `1709` | Windows 10 1709 | `16299` |
| `1803` | Windows 10 1803 | `17134` |
| `1809` | Windows 10 1809 | `17763` |
| `1903` | Windows 10 1903 | `18362` |
| `1909` | Windows 10 1909 | `18363` |
| `2004` | Windows 10 2004 | `19041` |
| `20H2` | Windows 10 20H2 | `19042` |
| `21H1` | Windows 10 21H1 | `19043` |
| `21H2` | Windows 10 21H2 | `19044` |
| `22H2` | Windows 10 22H2 | `19045` |
| `21H2` | Windows 11 21H2 | `22000` |
| `22H2` | Windows 11 22H2 | `22621` |
| `23H2` | Windows 11 23H2 | `22631` |
| `24H2` | Windows 11 24H2 | `26100` |
| `25H2` | Windows 11 25H2 | `26200` |
| `26H1` | Windows 11 26H1 | `28000` |