# Short circuit optimize
 * Short circuit optimize를 하는 AndAlso, OrElse와
 * 그렇지 않은 And, Or가 있다.

        Dim x1 As Boolean = t And f
        Dim x2 As Boolean = t AndAlso f
        Dim x3 As Boolean = t Or f
        Dim x4 As Boolean = t OrElse f
