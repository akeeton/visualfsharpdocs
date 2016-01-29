# Array.partition<'T> Function (F#)

Splits the collection into two collections, containing the elements for which the given predicate returns **true** and **false** respectively.

**Namespace/Module Path:** Microsoft.FSharp.Collections.Array

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## CAPS_SYNTAX_MD

```
// Signature:
Array.partition : ('T -> bool) -> 'T [] -> 'T [] * 'T []

// Usage:
Array.partition predicate array
```

#### CAPS_PARAMETERS_MD
*predicate*
Type: **'T -&gt;**[bool](http://msdn.microsoft.com/en-us/library/89c0cf9c-49ce-4207-a3be-555851a67dd5)


The function to test the input elements.


*array*
Type: **'T**[[]](http://msdn.microsoft.com/en-us/library/def20292-9aae-4596-9275-b94e594f8493)


The input array.



**A pair of arrays. The first containing the elements the predicate for which the predicate evaluated to true, and the second containing those for which the predicate evaluated to false.**
## CAPS_REMARKS_MD
This function is named **Partition** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following code illustrates the use of Array.partition.**
```

    let removeOutliers array1 min max =
        Array.partition (fun elem -> elem > min && elem < max) array1
        |> fst
    removeOutliers [| 1 .. 100 |] 50 60
    |> printf "%A"
```

**Output**
**[|51; 52; 53; 54; 55; 56; 57; 58; 59|]**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Array Module &#40;F&#35;&#41;](Collections.Array+Module+%28F%23%29.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+%28F%23%29.md)
