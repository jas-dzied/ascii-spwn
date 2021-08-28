# ascii-spwn
A small library to convert a character to its ASCII number.

# Usage
the library returns a single type, `converter`, which you can use to perform your conversions. To create a converter, you can use `@converter::new({path to ascii source})`. 

Your ascii source file must be in the format:

```
{decimal} {octal} {hexadecimal} {character} {html value} {description}
...
```

where each element is seperated by a tab.

for example:

```
33	041	21	00100001	!	&#33;	 	Exclamation mark
```

an `ascii.txt` file is provided so you don't have to make your own.

Once you have created your converter, you can do:

```
converter.decimal('U') // 85
converter.binary('U') //  01010101
converter.hexadecimal('U') // 55
```
