```
========================================
 parse phase
----------------------------------------
========================================
 load phase
----------------------------------------
========================================
 eval-ir phase
----------------------------------------
[1] TOP_LEVEL: Entry[25909]
[2] TOP_LEVEL: Call[25910] app __x0__ = (InitializeHostDefinedRealm)
[3] InitializeHostDefinedRealm: Entry[20570]
[4] InitializeHostDefinedRealm: Call[20571] app __x0__ = (CreateRealm)
[5] CreateRealm: Entry[7066]
[6] CreateRealm: Normal[7067] let realmRec = REALM
[7] CreateRealm: Call[7070] app __x0__ = (CreateIntrinsics realmRec)
[8] CreateIntrinsics: Entry[6890]
[9] CreateIntrinsics: Normal[6891] let intrinsics = (new Record())
[10] CreateIntrinsics: Normal[6894] realmRec.Intrinsics = intrinsics
[11] CreateIntrinsics: Normal[6896] realmRec.Intrinsics = INTRINSICS
[12] CreateIntrinsics: Normal[6898] intrinsics = INTRINSICS
[13] CreateIntrinsics: Call[6892] app __x0__ = (AddRestrictedFunctionProperties intrinsics["%Function.prototype%"] realmRec)
[14] AddRestrictedFunctionProperties: Entry[172]
[15] AddRestrictedFunctionProperties: Normal[173] let thrower = realm.Intrinsics["%ThrowTypeError%"]
[16] AddRestrictedFunctionProperties: Call[176] app __x0__ = (DefinePropertyOrThrow F "caller" (new PropertyDescriptor("Get" -> thrower, "Set" -> thrower, "Enumerable" -> false, "Configurable" -> true)))
[17] DefinePropertyOrThrow: Entry[7579]
[18] DefinePropertyOrThrow: Normal[7580] assert (= (typeof O) Object)
[19] DefinePropertyOrThrow: Call[7583] app __x0__ = (IsPropertyKey P)
[20] IsPropertyKey: Entry[21126]
[21] IsPropertyKey: If[21127] (= (typeof argument) String)
[22] IsPropertyKey: Normal[21130] return true
<RETURN> true
[23] DefinePropertyOrThrow: Normal[7586] assert (= __x0__ true)
[24] DefinePropertyOrThrow: Call[7587] app __x1__ = (O.DefineOwnProperty O P desc)
[25] OrdinaryObject.DefineOwnProperty: Entry[23851]
[26] OrdinaryObject.DefineOwnProperty: Call[23852] app __x0__ = (OrdinaryDefineOwnProperty O P Desc)
[27] OrdinaryDefineOwnProperty: Entry[23715]
[28] OrdinaryDefineOwnProperty: Call[23716] app __x0__ = (O.GetOwnProperty O P)
[29] OrdinaryObject.GetOwnProperty: Entry[23863]
[30] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[31] OrdinaryGetOwnProperty: Entry[23788]
[32] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[33] IsPropertyKey: Entry[21126]
[34] IsPropertyKey: If[21127] (= (typeof argument) String)
[35] IsPropertyKey: Normal[21130] return true
<RETURN> true
[36] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[37] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[38] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[39] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[40] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[41] IsDataDescriptor: Entry[21031]
[42] IsDataDescriptor: If[21032] (= Desc undefined)
[43] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[44] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[45] OrdinaryGetOwnProperty: If[23803] __x1__
[46] OrdinaryGetOwnProperty: Call[23806] app __x2__ = (IsAccessorDescriptor X)
[47] IsAccessorDescriptor: Entry[20967]
[48] IsAccessorDescriptor: If[20968] (= Desc undefined)
[49] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[50] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[51] OrdinaryGetOwnProperty: Normal[23802] assert __x2__
[52] OrdinaryGetOwnProperty: Normal[23798] D.Get = X.Get
[53] OrdinaryGetOwnProperty: Normal[23794] D.Set = X.Set
[54] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[55] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[56] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #2 -> (TYPE = PropertyDescriptor) {
  "Get" -> #GLOBAL.ThrowTypeError
  "Enumerable" -> false
  "Configurable" -> true
  "Set" -> #GLOBAL.ThrowTypeError
}
[57] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #2 -> (TYPE = PropertyDescriptor) {
  "Get" -> #GLOBAL.ThrowTypeError
  "Enumerable" -> false
  "Configurable" -> true
  "Set" -> #GLOBAL.ThrowTypeError
}
[58] OrdinaryDefineOwnProperty: Normal[23719] let current = [? __x0__]
[59] OrdinaryDefineOwnProperty: Call[23721] app __x1__ = (IsExtensible O)
[60] IsExtensible: Entry[21043]
[61] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[62] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[63] OrdinaryObject.IsExtensible: Entry[23875]
[64] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[65] OrdinaryIsExtensible: Entry[23848]
[66] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[67] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[68] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[69] OrdinaryDefineOwnProperty: Normal[23722] let extensible = [? __x1__]
[70] OrdinaryDefineOwnProperty: Call[23717] app __x2__ = (ValidateAndApplyPropertyDescriptor O P extensible Desc current)
[71] ValidateAndApplyPropertyDescriptor: Entry[28891]
[72] ValidateAndApplyPropertyDescriptor: If[28892] (= current undefined)
[73] ValidateAndApplyPropertyDescriptor: If[28938] (&& (= absent Desc.Value) (&& (= absent Desc.Writable) (&& (= absent Desc.Get) (&& (= absent Desc.Set) (&& (= absent Desc.Enumerable) (= absent Desc.Configurable))))))
[74] ValidateAndApplyPropertyDescriptor: If[28919] (= current.Configurable false)
[75] ValidateAndApplyPropertyDescriptor: Call[28898] app __x6__ = (IsGenericDescriptor Desc)
[76] IsGenericDescriptor: Entry[21048]
[77] IsGenericDescriptor: If[21049] (= Desc undefined)
[78] IsGenericDescriptor: Call[21054] app __x0__ = (IsAccessorDescriptor Desc)
[79] IsAccessorDescriptor: Entry[20967]
[80] IsAccessorDescriptor: If[20968] (= Desc undefined)
[81] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[82] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[83] IsGenericDescriptor: Call[21056] app __x1__ = (IsDataDescriptor Desc)
[84] IsDataDescriptor: Entry[21031]
[85] IsDataDescriptor: If[21032] (= Desc undefined)
[86] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[87] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[88] IsGenericDescriptor: If[21050] (&& (= __x0__ false) (= __x1__ false))
[89] IsGenericDescriptor: Normal[21052] return false
<RETURN> false
[90] ValidateAndApplyPropertyDescriptor: If[28923] (= [! __x6__] true)
[91] ValidateAndApplyPropertyDescriptor: Call[28973] app __x7__ = (IsDataDescriptor current)
[92] IsDataDescriptor: Entry[21031]
[93] IsDataDescriptor: If[21032] (= Desc undefined)
[94] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[95] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[96] ValidateAndApplyPropertyDescriptor: Call[28942] app __x8__ = (IsDataDescriptor Desc)
[97] IsDataDescriptor: Entry[21031]
[98] IsDataDescriptor: If[21032] (= Desc undefined)
[99] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[100] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[101] ValidateAndApplyPropertyDescriptor: Call[28934] app __x9__ = (SameValue [! __x7__] [! __x8__])
[102] SameValue: Entry[25946]
[103] SameValue: If[25947] (! (= (typeof x) (typeof y)))
[104] SameValue: If[25951] (|| (= (typeof x) Number) (= (typeof x) BigInt))
[105] SameValue: Call[25949] app __x1__ = (SameValueNonNumeric x y)
[106] SameValueNonNumeric: Entry[25955]
[107] SameValueNonNumeric: Normal[25956] assert (! (|| (= (typeof x) Number) (= (typeof x) BigInt)))
[108] SameValueNonNumeric: Normal[25966] assert (= (typeof x) (typeof y))
[109] SameValueNonNumeric: If[25970] (= (typeof x) Undefined)
[110] SameValueNonNumeric: If[25957] (= (typeof x) Null)
[111] SameValueNonNumeric: If[25959] (= (typeof x) String)
[112] SameValueNonNumeric: If[25967] (= (typeof x) Boolean)
[113] SameValueNonNumeric: If[25960] (|| (&& (= x true) (= y true)) (&& (= x false) (= y false)))
[114] SameValueNonNumeric: Normal[25961] return true
<RETURN> true
[115] SameValue: Normal[25952] return [! __x1__]
<RETURN> true
[116] ValidateAndApplyPropertyDescriptor: If[28935] (= [! __x9__] false)
[117] ValidateAndApplyPropertyDescriptor: Call[28962] app __x11__ = (IsDataDescriptor current)
[118] IsDataDescriptor: Entry[21031]
[119] IsDataDescriptor: If[21032] (= Desc undefined)
[120] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[121] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[122] ValidateAndApplyPropertyDescriptor: Call[28939] app __x12__ = (IsDataDescriptor Desc)
[123] IsDataDescriptor: Entry[21031]
[124] IsDataDescriptor: If[21032] (= Desc undefined)
[125] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[126] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[127] ValidateAndApplyPropertyDescriptor: If[28940] (&& (= __x11__ true) (= __x12__ true))
[128] ValidateAndApplyPropertyDescriptor: Call[28996] app __x15__ = (IsAccessorDescriptor current)
[129] IsAccessorDescriptor: Entry[20967]
[130] IsAccessorDescriptor: If[20968] (= Desc undefined)
[131] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[132] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[133] ValidateAndApplyPropertyDescriptor: Call[28893] app __x16__ = (IsAccessorDescriptor Desc)
[134] IsAccessorDescriptor: Entry[20967]
[135] IsAccessorDescriptor: If[20968] (= Desc undefined)
[136] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[137] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[138] ValidateAndApplyPropertyDescriptor: Normal[28894] assert (&& (= [! __x15__] true) (= [! __x16__] true))
[139] ValidateAndApplyPropertyDescriptor: If[28936] (= current.Configurable false)
[140] ValidateAndApplyPropertyDescriptor: If[28888] (! (= O undefined))
[141] ValidateAndApplyPropertyDescriptor: Normal[28929] let __keys__ = (map-keys Desc)
[142] ValidateAndApplyPropertyDescriptor: Normal[28987] let __i__ = 0i
[143] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[144] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[145] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[146] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[147] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[148] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[149] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[150] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[151] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[152] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[153] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[154] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[155] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[156] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[157] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[158] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[159] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[160] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[161] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[162] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[163] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[164] ValidateAndApplyPropertyDescriptor: Normal[28930] return true
<RETURN> true
[165] OrdinaryDefineOwnProperty: Normal[23718] return __x2__
<RETURN> N(true)
[166] OrdinaryObject.DefineOwnProperty: Normal[23853] return [? __x0__]
<RETURN> true
[167] DefinePropertyOrThrow: Normal[7581] let success = [? __x1__]
[168] DefinePropertyOrThrow: If[7582] (= success false)
[169] DefinePropertyOrThrow: Normal[7585] return success
<RETURN> true
[170] AddRestrictedFunctionProperties: Normal[177] [! __x0__]
[171] AddRestrictedFunctionProperties: Call[178] app __x1__ = (DefinePropertyOrThrow F "arguments" (new PropertyDescriptor("Get" -> thrower, "Set" -> thrower, "Enumerable" -> false, "Configurable" -> true)))
[172] DefinePropertyOrThrow: Entry[7579]
[173] DefinePropertyOrThrow: Normal[7580] assert (= (typeof O) Object)
[174] DefinePropertyOrThrow: Call[7583] app __x0__ = (IsPropertyKey P)
[175] IsPropertyKey: Entry[21126]
[176] IsPropertyKey: If[21127] (= (typeof argument) String)
[177] IsPropertyKey: Normal[21130] return true
<RETURN> true
[178] DefinePropertyOrThrow: Normal[7586] assert (= __x0__ true)
[179] DefinePropertyOrThrow: Call[7587] app __x1__ = (O.DefineOwnProperty O P desc)
[180] OrdinaryObject.DefineOwnProperty: Entry[23851]
[181] OrdinaryObject.DefineOwnProperty: Call[23852] app __x0__ = (OrdinaryDefineOwnProperty O P Desc)
[182] OrdinaryDefineOwnProperty: Entry[23715]
[183] OrdinaryDefineOwnProperty: Call[23716] app __x0__ = (O.GetOwnProperty O P)
[184] OrdinaryObject.GetOwnProperty: Entry[23863]
[185] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[186] OrdinaryGetOwnProperty: Entry[23788]
[187] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[188] IsPropertyKey: Entry[21126]
[189] IsPropertyKey: If[21127] (= (typeof argument) String)
[190] IsPropertyKey: Normal[21130] return true
<RETURN> true
[191] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[192] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[193] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[194] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[195] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[196] IsDataDescriptor: Entry[21031]
[197] IsDataDescriptor: If[21032] (= Desc undefined)
[198] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[199] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[200] OrdinaryGetOwnProperty: If[23803] __x1__
[201] OrdinaryGetOwnProperty: Call[23806] app __x2__ = (IsAccessorDescriptor X)
[202] IsAccessorDescriptor: Entry[20967]
[203] IsAccessorDescriptor: If[20968] (= Desc undefined)
[204] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[205] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[206] OrdinaryGetOwnProperty: Normal[23802] assert __x2__
[207] OrdinaryGetOwnProperty: Normal[23798] D.Get = X.Get
[208] OrdinaryGetOwnProperty: Normal[23794] D.Set = X.Set
[209] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[210] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[211] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #5 -> (TYPE = PropertyDescriptor) {
  "Get" -> #GLOBAL.ThrowTypeError
  "Enumerable" -> false
  "Configurable" -> true
  "Set" -> #GLOBAL.ThrowTypeError
}
[212] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #5 -> (TYPE = PropertyDescriptor) {
  "Get" -> #GLOBAL.ThrowTypeError
  "Enumerable" -> false
  "Configurable" -> true
  "Set" -> #GLOBAL.ThrowTypeError
}
[213] OrdinaryDefineOwnProperty: Normal[23719] let current = [? __x0__]
[214] OrdinaryDefineOwnProperty: Call[23721] app __x1__ = (IsExtensible O)
[215] IsExtensible: Entry[21043]
[216] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[217] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[218] OrdinaryObject.IsExtensible: Entry[23875]
[219] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[220] OrdinaryIsExtensible: Entry[23848]
[221] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[222] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[223] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[224] OrdinaryDefineOwnProperty: Normal[23722] let extensible = [? __x1__]
[225] OrdinaryDefineOwnProperty: Call[23717] app __x2__ = (ValidateAndApplyPropertyDescriptor O P extensible Desc current)
[226] ValidateAndApplyPropertyDescriptor: Entry[28891]
[227] ValidateAndApplyPropertyDescriptor: If[28892] (= current undefined)
[228] ValidateAndApplyPropertyDescriptor: If[28938] (&& (= absent Desc.Value) (&& (= absent Desc.Writable) (&& (= absent Desc.Get) (&& (= absent Desc.Set) (&& (= absent Desc.Enumerable) (= absent Desc.Configurable))))))
[229] ValidateAndApplyPropertyDescriptor: If[28919] (= current.Configurable false)
[230] ValidateAndApplyPropertyDescriptor: Call[28898] app __x6__ = (IsGenericDescriptor Desc)
[231] IsGenericDescriptor: Entry[21048]
[232] IsGenericDescriptor: If[21049] (= Desc undefined)
[233] IsGenericDescriptor: Call[21054] app __x0__ = (IsAccessorDescriptor Desc)
[234] IsAccessorDescriptor: Entry[20967]
[235] IsAccessorDescriptor: If[20968] (= Desc undefined)
[236] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[237] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[238] IsGenericDescriptor: Call[21056] app __x1__ = (IsDataDescriptor Desc)
[239] IsDataDescriptor: Entry[21031]
[240] IsDataDescriptor: If[21032] (= Desc undefined)
[241] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[242] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[243] IsGenericDescriptor: If[21050] (&& (= __x0__ false) (= __x1__ false))
[244] IsGenericDescriptor: Normal[21052] return false
<RETURN> false
[245] ValidateAndApplyPropertyDescriptor: If[28923] (= [! __x6__] true)
[246] ValidateAndApplyPropertyDescriptor: Call[28973] app __x7__ = (IsDataDescriptor current)
[247] IsDataDescriptor: Entry[21031]
[248] IsDataDescriptor: If[21032] (= Desc undefined)
[249] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[250] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[251] ValidateAndApplyPropertyDescriptor: Call[28942] app __x8__ = (IsDataDescriptor Desc)
[252] IsDataDescriptor: Entry[21031]
[253] IsDataDescriptor: If[21032] (= Desc undefined)
[254] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[255] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[256] ValidateAndApplyPropertyDescriptor: Call[28934] app __x9__ = (SameValue [! __x7__] [! __x8__])
[257] SameValue: Entry[25946]
[258] SameValue: If[25947] (! (= (typeof x) (typeof y)))
[259] SameValue: If[25951] (|| (= (typeof x) Number) (= (typeof x) BigInt))
[260] SameValue: Call[25949] app __x1__ = (SameValueNonNumeric x y)
[261] SameValueNonNumeric: Entry[25955]
[262] SameValueNonNumeric: Normal[25956] assert (! (|| (= (typeof x) Number) (= (typeof x) BigInt)))
[263] SameValueNonNumeric: Normal[25966] assert (= (typeof x) (typeof y))
[264] SameValueNonNumeric: If[25970] (= (typeof x) Undefined)
[265] SameValueNonNumeric: If[25957] (= (typeof x) Null)
[266] SameValueNonNumeric: If[25959] (= (typeof x) String)
[267] SameValueNonNumeric: If[25967] (= (typeof x) Boolean)
[268] SameValueNonNumeric: If[25960] (|| (&& (= x true) (= y true)) (&& (= x false) (= y false)))
[269] SameValueNonNumeric: Normal[25961] return true
<RETURN> true
[270] SameValue: Normal[25952] return [! __x1__]
<RETURN> true
[271] ValidateAndApplyPropertyDescriptor: If[28935] (= [! __x9__] false)
[272] ValidateAndApplyPropertyDescriptor: Call[28962] app __x11__ = (IsDataDescriptor current)
[273] IsDataDescriptor: Entry[21031]
[274] IsDataDescriptor: If[21032] (= Desc undefined)
[275] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[276] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[277] ValidateAndApplyPropertyDescriptor: Call[28939] app __x12__ = (IsDataDescriptor Desc)
[278] IsDataDescriptor: Entry[21031]
[279] IsDataDescriptor: If[21032] (= Desc undefined)
[280] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[281] IsDataDescriptor: Normal[21037] return false
<RETURN> false
[282] ValidateAndApplyPropertyDescriptor: If[28940] (&& (= __x11__ true) (= __x12__ true))
[283] ValidateAndApplyPropertyDescriptor: Call[28996] app __x15__ = (IsAccessorDescriptor current)
[284] IsAccessorDescriptor: Entry[20967]
[285] IsAccessorDescriptor: If[20968] (= Desc undefined)
[286] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[287] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[288] ValidateAndApplyPropertyDescriptor: Call[28893] app __x16__ = (IsAccessorDescriptor Desc)
[289] IsAccessorDescriptor: Entry[20967]
[290] IsAccessorDescriptor: If[20968] (= Desc undefined)
[291] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[292] IsAccessorDescriptor: Normal[20969] return true
<RETURN> true
[293] ValidateAndApplyPropertyDescriptor: Normal[28894] assert (&& (= [! __x15__] true) (= [! __x16__] true))
[294] ValidateAndApplyPropertyDescriptor: If[28936] (= current.Configurable false)
[295] ValidateAndApplyPropertyDescriptor: If[28888] (! (= O undefined))
[296] ValidateAndApplyPropertyDescriptor: Normal[28929] let __keys__ = (map-keys Desc)
[297] ValidateAndApplyPropertyDescriptor: Normal[28987] let __i__ = 0i
[298] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[299] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[300] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[301] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[302] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[303] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[304] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[305] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[306] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[307] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[308] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[309] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[310] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[311] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[312] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[313] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[314] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[315] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[316] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[317] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[318] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[319] ValidateAndApplyPropertyDescriptor: Normal[28930] return true
<RETURN> true
[320] OrdinaryDefineOwnProperty: Normal[23718] return __x2__
<RETURN> N(true)
[321] OrdinaryObject.DefineOwnProperty: Normal[23853] return [? __x0__]
<RETURN> true
[322] DefinePropertyOrThrow: Normal[7581] let success = [? __x1__]
[323] DefinePropertyOrThrow: If[7582] (= success false)
[324] DefinePropertyOrThrow: Normal[7585] return success
<RETURN> true
[325] AddRestrictedFunctionProperties: Normal[174] return [! __x1__]
<RETURN> true
[326] CreateIntrinsics: Normal[6893] __x0__
[327] CreateIntrinsics: Normal[6895] return intrinsics
<RETURN> #INTRINSICS -> (TYPE = INTRINSICS) {}
[328] CreateRealm: Normal[7072] __x0__
[329] CreateRealm: Normal[7074] realmRec.GlobalObject = undefined
[330] CreateRealm: Normal[7068] realmRec.GlobalEnv = undefined
[331] CreateRealm: Normal[7069] realmRec.TemplateMap = (new [])
[332] CreateRealm: Normal[7071] return realmRec
<RETURN> #REALM -> (TYPE = RealmRecord) {
  "TemplateMap" -> #7
  "GlobalObject" -> undefined
  "GlobalEnv" -> undefined
  "Intrinsics" -> #INTRINSICS
  "SubMap" -> #REALM.SubMap
}
[333] InitializeHostDefinedRealm: Normal[20578] let realm = __x0__
[334] InitializeHostDefinedRealm: Normal[20582] let newContext = (new ExecutionContext())
[335] InitializeHostDefinedRealm: Normal[20585] newContext.Function = null
[336] InitializeHostDefinedRealm: Normal[20572] newContext.Realm = realm
[337] InitializeHostDefinedRealm: Normal[20573] newContext.ScriptOrModule = null
[338] InitializeHostDefinedRealm: Normal[20579] append newContext -> EXECUTION_STACK
[339] InitializeHostDefinedRealm: Normal[20584] CONTEXT = EXECUTION_STACK[(- EXECUTION_STACK.length 1i)]
[340] InitializeHostDefinedRealm: Normal[20580] let global = undefined
[341] InitializeHostDefinedRealm: Normal[20574] let thisValue = undefined
[342] InitializeHostDefinedRealm: Call[20575] app __x1__ = (SetRealmGlobalObject realm global thisValue)
[343] SetRealmGlobalObject: Entry[26307]
[344] SetRealmGlobalObject: If[26308] (= globalObj undefined)
[345] SetRealmGlobalObject: Normal[26313] let intrinsics = realmRec.Intrinsics
[346] SetRealmGlobalObject: Call[26317] app __x0__ = (OrdinaryObjectCreate intrinsics["%Object.prototype%"])
[347] OrdinaryObjectCreate: Entry[23895]
[348] OrdinaryObjectCreate: Normal[23896] let internalSlotsList = (new ["Prototype", "Extensible"])
[349] OrdinaryObjectCreate: If[23901] (! (= additionalInternalSlotsList absent))
[350] OrdinaryObjectCreate: Call[23899] app __x3__ = (MakeBasicObject internalSlotsList)
[351] MakeBasicObject: Entry[21819]
[352] MakeBasicObject: Normal[21820] let obj = (new OrdinaryObject())
[353] MakeBasicObject: Normal[21825] let __x0__ = internalSlotsList
[354] MakeBasicObject: Normal[21828] let __x1__ = 0i
[355] MakeBasicObject: Loop[21830] (< __x1__ __x0__.length)
[356] MakeBasicObject: Normal[21821] let __x2__ = __x0__[__x1__]
[357] MakeBasicObject: Normal[21822] __x1__ = (+ __x1__ 1i)
[358] MakeBasicObject: Normal[21826] obj[__x2__] = undefined
[359] MakeBasicObject: LoopCont[21829]
[360] MakeBasicObject: Loop[21830] (< __x1__ __x0__.length)
[361] MakeBasicObject: Normal[21821] let __x2__ = __x0__[__x1__]
[362] MakeBasicObject: Normal[21822] __x1__ = (+ __x1__ 1i)
[363] MakeBasicObject: Normal[21826] obj[__x2__] = undefined
[364] MakeBasicObject: LoopCont[21829]
[365] MakeBasicObject: Loop[21830] (< __x1__ __x0__.length)
[366] MakeBasicObject: If[21827] (contains internalSlotsList "Extensible")
[367] MakeBasicObject: Normal[21823] obj.Extensible = true
[368] MakeBasicObject: Normal[21824] return obj
<RETURN> #11 -> (TYPE = OrdinaryObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> undefined
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "SubMap" -> #10
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[369] OrdinaryObjectCreate: Normal[23900] let O = [! __x3__]
[370] OrdinaryObjectCreate: Normal[23907] O.Prototype = proto
[371] OrdinaryObjectCreate: Normal[23904] return O
<RETURN> #11 -> (TYPE = OrdinaryObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Object.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "SubMap" -> #10
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[372] SetRealmGlobalObject: Normal[26320] globalObj = [! __x0__]
[373] SetRealmGlobalObject: Normal[26309] assert (= (typeof globalObj) Object)
[374] SetRealmGlobalObject: If[26310] (= thisValue undefined)
[375] SetRealmGlobalObject: Normal[26314] thisValue = globalObj
[376] SetRealmGlobalObject: Normal[26315] realmRec.GlobalObject = globalObj
[377] SetRealmGlobalObject: Call[26316] app __x1__ = (NewGlobalEnvironment globalObj thisValue)
[378] NewGlobalEnvironment: Entry[22931]
[379] NewGlobalEnvironment: Normal[22932] let objRec = (new ObjectEnvironmentRecord("BindingObject" -> G, "withEnvironment" -> false))
[380] NewGlobalEnvironment: Normal[22935] let dclRec = (new DeclarativeEnvironmentRecord())
[381] NewGlobalEnvironment: Normal[22939] let env = (new GlobalEnvironmentRecord())
[382] NewGlobalEnvironment: Normal[22941] env.ObjectRecord = objRec
[383] NewGlobalEnvironment: Normal[22933] env.GlobalThisValue = thisValue
[384] NewGlobalEnvironment: Normal[22934] env.DeclarativeRecord = dclRec
[385] NewGlobalEnvironment: Normal[22936] env.VarNames = (new [])
[386] NewGlobalEnvironment: Normal[22940] env.OuterEnv = null
[387] NewGlobalEnvironment: Normal[22937] return env
<RETURN> #17 -> (TYPE = GlobalEnvironmentRecord) {
  "WithBaseObject" -> λ(GlobalEnvironmentRecord.WithBaseObject)
  "DeleteBinding" -> λ(GlobalEnvironmentRecord.DeleteBinding)
  "CreateMutableBinding" -> λ(GlobalEnvironmentRecord.CreateMutableBinding)
  "HasRestrictedGlobalProperty" -> λ(GlobalEnvironmentRecord.HasRestrictedGlobalProperty)
  "CreateGlobalFunctionBinding" -> λ(GlobalEnvironmentRecord.CreateGlobalFunctionBinding)
  "GetBindingValue" -> λ(GlobalEnvironmentRecord.GetBindingValue)
  "CreateGlobalVarBinding" -> λ(GlobalEnvironmentRecord.CreateGlobalVarBinding)
  "HasLexicalDeclaration" -> λ(GlobalEnvironmentRecord.HasLexicalDeclaration)
  "OuterEnv" -> null
  "VarNames" -> #18
  "HasSuperBinding" -> λ(GlobalEnvironmentRecord.HasSuperBinding)
  "GetThisBinding" -> λ(GlobalEnvironmentRecord.GetThisBinding)
  "CanDeclareGlobalFunction" -> λ(GlobalEnvironmentRecord.CanDeclareGlobalFunction)
  "DeclarativeRecord" -> #15
  "InitializeBinding" -> λ(GlobalEnvironmentRecord.InitializeBinding)
  "CreateImmutableBinding" -> λ(GlobalEnvironmentRecord.CreateImmutableBinding)
  "ObjectRecord" -> #13
  "HasThisBinding" -> λ(GlobalEnvironmentRecord.HasThisBinding)
  "SetMutableBinding" -> λ(GlobalEnvironmentRecord.SetMutableBinding)
  "HasBinding" -> λ(GlobalEnvironmentRecord.HasBinding)
  "CanDeclareGlobalVar" -> λ(GlobalEnvironmentRecord.CanDeclareGlobalVar)
  "GlobalThisValue" -> #11
  "SubMap" -> #16
  "HasVarDeclaration" -> λ(GlobalEnvironmentRecord.HasVarDeclaration)
}
[388] SetRealmGlobalObject: Normal[26311] let newGlobalEnv = __x1__
[389] SetRealmGlobalObject: Normal[26312] realmRec.GlobalEnv = newGlobalEnv
[390] SetRealmGlobalObject: Normal[26318] return realmRec
<RETURN> N(#REALM) -> (TYPE = RealmRecord) {
  "TemplateMap" -> #7
  "GlobalObject" -> #11
  "GlobalEnv" -> N(#17)
  "Intrinsics" -> #INTRINSICS
  "SubMap" -> #REALM.SubMap
}
[391] InitializeHostDefinedRealm: Normal[20583] __x1__
[392] InitializeHostDefinedRealm: Call[20581] app __x2__ = (SetDefaultGlobalBindings realm)
[393] SetDefaultGlobalBindings: Entry[26231]
[394] SetDefaultGlobalBindings: Normal[26232] let global = realmRec.GlobalObject
[395] SetDefaultGlobalBindings: Normal[26237] let __keys__ = (map-keys GLOBAL.SubMap)
[396] SetDefaultGlobalBindings: Normal[26241] let __i__ = 0i
[397] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[398] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[399] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[400] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[401] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[402] SetDefaultGlobalBindings: LoopCont[26239]
[403] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[404] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[405] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[406] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[407] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[408] SetDefaultGlobalBindings: LoopCont[26239]
[409] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[410] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[411] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[412] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[413] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[414] SetDefaultGlobalBindings: LoopCont[26239]
[415] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[416] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[417] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[418] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[419] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[420] SetDefaultGlobalBindings: LoopCont[26239]
[421] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[422] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[423] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[424] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[425] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[426] SetDefaultGlobalBindings: LoopCont[26239]
[427] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[428] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[429] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[430] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[431] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[432] SetDefaultGlobalBindings: LoopCont[26239]
[433] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[434] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[435] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[436] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[437] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[438] SetDefaultGlobalBindings: LoopCont[26239]
[439] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[440] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[441] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[442] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[443] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[444] SetDefaultGlobalBindings: LoopCont[26239]
[445] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[446] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[447] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[448] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[449] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[450] SetDefaultGlobalBindings: LoopCont[26239]
[451] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[452] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[453] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[454] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[455] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[456] SetDefaultGlobalBindings: LoopCont[26239]
[457] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[458] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[459] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[460] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[461] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[462] SetDefaultGlobalBindings: LoopCont[26239]
[463] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[464] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[465] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[466] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[467] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[468] SetDefaultGlobalBindings: LoopCont[26239]
[469] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[470] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[471] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[472] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[473] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[474] SetDefaultGlobalBindings: LoopCont[26239]
[475] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[476] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[477] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[478] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[479] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[480] SetDefaultGlobalBindings: LoopCont[26239]
[481] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[482] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[483] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[484] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[485] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[486] SetDefaultGlobalBindings: LoopCont[26239]
[487] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[488] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[489] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[490] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[491] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[492] SetDefaultGlobalBindings: LoopCont[26239]
[493] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[494] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[495] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[496] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[497] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[498] SetDefaultGlobalBindings: LoopCont[26239]
[499] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[500] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[501] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[502] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[503] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[504] SetDefaultGlobalBindings: LoopCont[26239]
[505] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[506] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[507] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[508] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[509] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[510] SetDefaultGlobalBindings: LoopCont[26239]
[511] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[512] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[513] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[514] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[515] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[516] SetDefaultGlobalBindings: LoopCont[26239]
[517] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[518] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[519] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[520] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[521] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[522] SetDefaultGlobalBindings: LoopCont[26239]
[523] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[524] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[525] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[526] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[527] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[528] SetDefaultGlobalBindings: LoopCont[26239]
[529] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[530] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[531] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[532] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[533] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[534] SetDefaultGlobalBindings: LoopCont[26239]
[535] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[536] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[537] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[538] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[539] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[540] SetDefaultGlobalBindings: LoopCont[26239]
[541] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[542] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[543] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[544] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[545] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[546] SetDefaultGlobalBindings: LoopCont[26239]
[547] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[548] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[549] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[550] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[551] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[552] SetDefaultGlobalBindings: LoopCont[26239]
[553] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[554] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[555] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[556] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[557] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[558] SetDefaultGlobalBindings: LoopCont[26239]
[559] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[560] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[561] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[562] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[563] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[564] SetDefaultGlobalBindings: LoopCont[26239]
[565] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[566] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[567] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[568] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[569] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[570] SetDefaultGlobalBindings: LoopCont[26239]
[571] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[572] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[573] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[574] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[575] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[576] SetDefaultGlobalBindings: LoopCont[26239]
[577] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[578] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[579] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[580] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[581] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[582] SetDefaultGlobalBindings: LoopCont[26239]
[583] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[584] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[585] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[586] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[587] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[588] SetDefaultGlobalBindings: LoopCont[26239]
[589] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[590] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[591] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[592] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[593] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[594] SetDefaultGlobalBindings: LoopCont[26239]
[595] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[596] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[597] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[598] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[599] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[600] SetDefaultGlobalBindings: LoopCont[26239]
[601] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[602] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[603] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[604] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[605] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[606] SetDefaultGlobalBindings: LoopCont[26239]
[607] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[608] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[609] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[610] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[611] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[612] SetDefaultGlobalBindings: LoopCont[26239]
[613] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[614] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[615] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[616] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[617] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[618] SetDefaultGlobalBindings: LoopCont[26239]
[619] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[620] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[621] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[622] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[623] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[624] SetDefaultGlobalBindings: LoopCont[26239]
[625] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[626] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[627] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[628] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[629] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[630] SetDefaultGlobalBindings: LoopCont[26239]
[631] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[632] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[633] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[634] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[635] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[636] SetDefaultGlobalBindings: LoopCont[26239]
[637] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[638] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[639] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[640] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[641] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[642] SetDefaultGlobalBindings: LoopCont[26239]
[643] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[644] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[645] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[646] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[647] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[648] SetDefaultGlobalBindings: LoopCont[26239]
[649] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[650] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[651] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[652] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[653] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[654] SetDefaultGlobalBindings: LoopCont[26239]
[655] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[656] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[657] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[658] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[659] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[660] SetDefaultGlobalBindings: LoopCont[26239]
[661] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[662] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[663] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[664] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[665] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[666] SetDefaultGlobalBindings: LoopCont[26239]
[667] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[668] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[669] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[670] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[671] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[672] SetDefaultGlobalBindings: LoopCont[26239]
[673] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[674] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[675] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[676] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[677] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[678] SetDefaultGlobalBindings: LoopCont[26239]
[679] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[680] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[681] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[682] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[683] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[684] SetDefaultGlobalBindings: LoopCont[26239]
[685] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[686] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[687] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[688] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[689] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[690] SetDefaultGlobalBindings: LoopCont[26239]
[691] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[692] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[693] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[694] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[695] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[696] SetDefaultGlobalBindings: LoopCont[26239]
[697] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[698] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[699] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[700] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[701] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[702] SetDefaultGlobalBindings: LoopCont[26239]
[703] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[704] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[705] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[706] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[707] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[708] SetDefaultGlobalBindings: LoopCont[26239]
[709] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[710] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[711] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[712] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[713] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[714] SetDefaultGlobalBindings: LoopCont[26239]
[715] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[716] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[717] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[718] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[719] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[720] SetDefaultGlobalBindings: LoopCont[26239]
[721] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[722] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[723] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[724] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[725] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[726] SetDefaultGlobalBindings: LoopCont[26239]
[727] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[728] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[729] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[730] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[731] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[732] SetDefaultGlobalBindings: LoopCont[26239]
[733] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[734] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[735] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[736] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[737] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[738] SetDefaultGlobalBindings: LoopCont[26239]
[739] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[740] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[741] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[742] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[743] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[744] SetDefaultGlobalBindings: LoopCont[26239]
[745] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[746] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[747] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[748] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[749] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[750] SetDefaultGlobalBindings: LoopCont[26239]
[751] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[752] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[753] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[754] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[755] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[756] SetDefaultGlobalBindings: LoopCont[26239]
[757] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[758] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[759] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[760] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[761] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[762] SetDefaultGlobalBindings: LoopCont[26239]
[763] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[764] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[765] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[766] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[767] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[768] SetDefaultGlobalBindings: LoopCont[26239]
[769] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[770] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[771] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[772] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[773] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[774] SetDefaultGlobalBindings: LoopCont[26239]
[775] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[776] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[777] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[778] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[779] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[780] SetDefaultGlobalBindings: LoopCont[26239]
[781] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[782] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[783] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[784] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[785] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[786] SetDefaultGlobalBindings: LoopCont[26239]
[787] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[788] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[789] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[790] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[791] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[792] SetDefaultGlobalBindings: LoopCont[26239]
[793] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[794] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[795] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[796] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[797] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[798] SetDefaultGlobalBindings: LoopCont[26239]
[799] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[800] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[801] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[802] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[803] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[804] SetDefaultGlobalBindings: LoopCont[26239]
[805] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[806] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[807] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[808] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[809] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[810] SetDefaultGlobalBindings: LoopCont[26239]
[811] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[812] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[813] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[814] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[815] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[816] SetDefaultGlobalBindings: LoopCont[26239]
[817] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[818] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[819] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[820] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[821] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[822] SetDefaultGlobalBindings: LoopCont[26239]
[823] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[824] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[825] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[826] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[827] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[828] SetDefaultGlobalBindings: LoopCont[26239]
[829] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[830] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[831] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[832] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[833] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[834] SetDefaultGlobalBindings: LoopCont[26239]
[835] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[836] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[837] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[838] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[839] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[840] SetDefaultGlobalBindings: LoopCont[26239]
[841] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[842] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[843] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[844] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[845] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[846] SetDefaultGlobalBindings: LoopCont[26239]
[847] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[848] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[849] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[850] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[851] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[852] SetDefaultGlobalBindings: LoopCont[26239]
[853] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[854] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[855] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[856] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[857] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[858] SetDefaultGlobalBindings: LoopCont[26239]
[859] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[860] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[861] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[862] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[863] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[864] SetDefaultGlobalBindings: LoopCont[26239]
[865] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[866] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[867] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[868] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[869] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[870] SetDefaultGlobalBindings: LoopCont[26239]
[871] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[872] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[873] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[874] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[875] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[876] SetDefaultGlobalBindings: LoopCont[26239]
[877] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[878] SetDefaultGlobalBindings: Normal[26233] let name = __keys__[__i__]
[879] SetDefaultGlobalBindings: Normal[26234] let desc = GLOBAL.SubMap[name]
[880] SetDefaultGlobalBindings: Normal[26238] global.SubMap[name] = GLOBAL.SubMap[name]
[881] SetDefaultGlobalBindings: Normal[26242] __i__ = (+ __i__ 1i)
[882] SetDefaultGlobalBindings: LoopCont[26239]
[883] SetDefaultGlobalBindings: Loop[26240] (< __i__ __keys__.length)
[884] SetDefaultGlobalBindings: Normal[26235] global.SubMap.globalThis.Value = global
[885] SetDefaultGlobalBindings: Normal[26236] return global
<RETURN> #11 -> (TYPE = OrdinaryObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Object.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "SubMap" -> #10
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[886] InitializeHostDefinedRealm: Normal[20576] let globalObj = [? __x2__]
[887] InitializeHostDefinedRealm: Normal[20577] return ~empty~
<RETURN> ~empty~
[888] TOP_LEVEL: Normal[25918] [? __x0__]
[889] TOP_LEVEL: Call[25922] app __x1__ = (EnqueueJob "ScriptJobs" ScriptEvaluationJob (new [SCRIPT_BODY, HOST_DEFINED]))
[890] EnqueueJob: Entry[7913]
[891] EnqueueJob: Normal[7914] let callerContext = CONTEXT
[892] EnqueueJob: Normal[7917] let callerRealm = callerContext.Realm
[893] EnqueueJob: Normal[7919] let callerScriptOrModule = callerContext.ScriptOrModule
[894] EnqueueJob: Normal[7920] let pending = (new PendingJob("Job" -> job, "Arguments" -> arguments, "Realm" -> callerRealm, "ScriptOrModule" -> callerScriptOrModule, "HostDefined" -> undefined))
[895] EnqueueJob: Normal[7915] append pending -> JOB_QUEUE
[896] EnqueueJob: Normal[7916] return ~empty~
<RETURN> ~empty~
[897] TOP_LEVEL: Loop[25926] true
[898] TOP_LEVEL: If[25911] (= EXECUTION_STACK[(- EXECUTION_STACK.length 1i)] CONTEXT)
[899] TOP_LEVEL: Normal[25912] let __x2__ = (- EXECUTION_STACK.length 1i)
[900] TOP_LEVEL: Normal[25919] (pop EXECUTION_STACK __x2__)
[901] TOP_LEVEL: If[25923] (= EXECUTION_STACK.length 0i)
[902] TOP_LEVEL: Normal[25920] CONTEXT = null
[903] TOP_LEVEL: If[25915] (= JOB_QUEUE.length 0.0)
[904] TOP_LEVEL: Normal[25916] let nextQueue = JOB_QUEUE
[905] TOP_LEVEL: Normal[25917] let nextPending = (pop nextQueue 0i)
[906] TOP_LEVEL: Normal[25928] let newContext = (new ExecutionContext("SubMap" -> (new SubMap())))
[907] TOP_LEVEL: Normal[25942] newContext.Function = null
[908] TOP_LEVEL: Normal[25924] newContext.Realm = nextPending.Realm
[909] TOP_LEVEL: Normal[25925] newContext.ScriptOrModule = nextPending.ScriptOrModule
[910] TOP_LEVEL: Normal[25933] append newContext -> EXECUTION_STACK
[911] TOP_LEVEL: Normal[25934] CONTEXT = EXECUTION_STACK[(- EXECUTION_STACK.length 1i)]
[912] TOP_LEVEL: Normal[25938] let job = nextPending.Job
[913] TOP_LEVEL: Normal[25944] let args = nextPending.Arguments
[914] TOP_LEVEL: If[25929] (= args absent)
[915] TOP_LEVEL: If[25931] (= args.length 1i)
[916] TOP_LEVEL: If[25936] (= args.length 2i)
[917] TOP_LEVEL: Call[25935] app __x3__ = (job args[0i] args[1i])
[918] ScriptEvaluationJob: Entry[26046]
[919] ScriptEvaluationJob: Normal[26047] let realm = REALM
[920] ScriptEvaluationJob: Call[26050] app scriptRecord = (ParseScript sourceText realm hostDefined)
[921] ParseScript: Entry[24089]
[922] ParseScript: Normal[24090] let body = sourceText
[923] ParseScript: Normal[24091] return (new ScriptRecord("Realm" -> realm, "Environment" -> undefined, "ECMAScriptCode" -> body, "HostDefined" -> hostDefined))
<RETURN> #24 -> (TYPE = ScriptRecord) {
  "Environment" -> undefined
  "ECMAScriptCode" -> ☊[ScriptBody](var x = 1 + 2 ; print ( x ) ;)
  "Realm" -> #REALM
  "HostDefined" -> undefined
}
[924] ScriptEvaluationJob: Call[26051] app __x1__ = (ScriptEvaluation scriptRecord)
[925] ScriptEvaluation: Entry[26019]
[926] ScriptEvaluation: Normal[26020] let globalEnv = scriptRecord.Realm.GlobalEnv
[927] ScriptEvaluation: Normal[26030] let scriptContext = (new ExecutionContext())
[928] ScriptEvaluation: Normal[26036] scriptContext.Function = null
[929] ScriptEvaluation: Normal[26040] scriptContext.Realm = scriptRecord.Realm
[930] ScriptEvaluation: Normal[26021] scriptContext.ScriptOrModule = scriptRecord
[931] ScriptEvaluation: Normal[26022] scriptContext.VariableEnvironment = globalEnv
[932] ScriptEvaluation: Normal[26031] scriptContext.LexicalEnvironment = globalEnv
[933] ScriptEvaluation: Normal[26039] CONTEXT = null
[934] ScriptEvaluation: Normal[26034] append scriptContext -> EXECUTION_STACK
[935] ScriptEvaluation: Normal[26023] CONTEXT = EXECUTION_STACK[(- EXECUTION_STACK.length 1i)]
[936] ScriptEvaluation: Normal[26024] let scriptBody = scriptRecord.ECMAScriptCode
[937] ScriptEvaluation: Call[26038] app __x0__ = (GlobalDeclarationInstantiation scriptBody globalEnv)
[938] GlobalDeclarationInstantiation: Entry[19608]
[939] GlobalDeclarationInstantiation: Normal[19609] assert (is-instance-of env GlobalEnvironmentRecord)
[940] GlobalDeclarationInstantiation: Call[19654] access __x0__ = (script "LexicallyDeclaredNames")
[941] ScriptBody[0,0].LexicallyDeclaredNames: Entry[25999]
[942] ScriptBody[0,0].LexicallyDeclaredNames: Normal[26000] let ScriptBody = this
[943] ScriptBody[0,0].LexicallyDeclaredNames: Call[26001] access __x0__ = (StatementList "TopLevelLexicallyDeclaredNames")
[944] StatementList[1,0].TopLevelLexicallyDeclaredNames: Entry[26917]
[945] StatementList[1,0].TopLevelLexicallyDeclaredNames: Call[26918] access __x0__ = (StatementList "TopLevelLexicallyDeclaredNames")
[946] StatementListItem[0,0].TopLevelLexicallyDeclaredNames: Entry[26758]
[947] StatementListItem[0,0].TopLevelLexicallyDeclaredNames: Normal[26759] let StatementListItem = this
[948] StatementListItem[0,0].TopLevelLexicallyDeclaredNames: Normal[26760] return (new [])
<RETURN> #26 -> []
[949] StatementList[1,0].TopLevelLexicallyDeclaredNames: Normal[26922] let names = __x0__
[950] StatementList[1,0].TopLevelLexicallyDeclaredNames: Call[26926] access __x1__ = (StatementListItem "TopLevelLexicallyDeclaredNames")
[951] StatementListItem[0,0].TopLevelLexicallyDeclaredNames: Entry[26758]
[952] StatementListItem[0,0].TopLevelLexicallyDeclaredNames: Normal[26759] let StatementListItem = this
[953] StatementListItem[0,0].TopLevelLexicallyDeclaredNames: Normal[26760] return (new [])
<RETURN> #27 -> []
[954] StatementList[1,0].TopLevelLexicallyDeclaredNames: Normal[26928] let __x2__ = __x1__
[955] StatementList[1,0].TopLevelLexicallyDeclaredNames: Normal[26919] let __x3__ = 0i
[956] StatementList[1,0].TopLevelLexicallyDeclaredNames: Loop[26920] (< __x3__ __x2__.length)
[957] StatementList[1,0].TopLevelLexicallyDeclaredNames: Normal[26924] return names
<RETURN> N(#26) -> []
[958] ScriptBody[0,0].LexicallyDeclaredNames: Normal[26002] return __x0__
<RETURN> N(#26) -> []
[959] GlobalDeclarationInstantiation: Normal[19683] let lexNames = __x0__
[960] GlobalDeclarationInstantiation: Call[19709] access __x1__ = (script "VarDeclaredNames")
[961] ScriptBody[0,0].VarDeclaredNames: Entry[26009]
[962] ScriptBody[0,0].VarDeclaredNames: Normal[26010] let ScriptBody = this
[963] ScriptBody[0,0].VarDeclaredNames: Call[26011] access __x0__ = (StatementList "TopLevelVarDeclaredNames")
[964] StatementList[1,0].TopLevelVarDeclaredNames: Entry[26943]
[965] StatementList[1,0].TopLevelVarDeclaredNames: Call[26944] access __x0__ = (StatementList "TopLevelVarDeclaredNames")
[966] StatementListItem[0,0].TopLevelVarDeclaredNames: Entry[26766]
[967] StatementListItem[0,0].TopLevelVarDeclaredNames: Normal[26767] let StatementListItem = this
[968] StatementListItem[0,0].TopLevelVarDeclaredNames: If[26770] (is-instance-of Statement Statement10)
[969] StatementListItem[0,0].TopLevelVarDeclaredNames: Call[26769] access __x1__ = (Statement "VarDeclaredNames")
[970] VariableStatement[0,0].VarDeclaredNames: Entry[29130]
[971] VariableStatement[0,0].VarDeclaredNames: Normal[29131] let VariableStatement = this
[972] VariableStatement[0,0].VarDeclaredNames: Call[29132] access __x0__ = (VariableDeclarationList "BoundNames")
[973] VariableDeclaration[0,1].BoundNames: Entry[29087]
[974] VariableDeclaration[0,1].BoundNames: Normal[29088] let VariableDeclaration = this
[975] VariableDeclaration[0,1].BoundNames: Call[29089] access __x0__ = (BindingIdentifier "BoundNames")
[976] BindingIdentifier[0,0].BoundNames: Entry[3476]
[977] BindingIdentifier[0,0].BoundNames: Normal[3477] let BindingIdentifier = this
[978] BindingIdentifier[0,0].BoundNames: Call[3478] access __x0__ = (Identifier "StringValue")
[979] Identifier[0,0].StringValue: Entry[20090]
[980] Identifier[0,0].StringValue: Normal[20091] let Identifier = this
[981] Identifier[0,0].StringValue: Call[20092] access __x0__ = (IdentifierName "StringValue")
[982] Identifier[0,0].StringValue: Normal[20093] return __x0__
<RETURN> "x"
[983] BindingIdentifier[0,0].BoundNames: Normal[3479] return (new [__x0__])
<RETURN> #28 -> ["x"]
[984] VariableDeclaration[0,1].BoundNames: Normal[29090] return __x0__
<RETURN> N(#28) -> ["x"]
[985] VariableStatement[0,0].VarDeclaredNames: Normal[29133] return __x0__
<RETURN> N(#28) -> ["x"]
[986] StatementListItem[0,0].TopLevelVarDeclaredNames: Normal[26771] return __x1__
<RETURN> N(#28) -> ["x"]
[987] StatementList[1,0].TopLevelVarDeclaredNames: Normal[26948] let names = __x0__
[988] StatementList[1,0].TopLevelVarDeclaredNames: Call[26952] access __x1__ = (StatementListItem "TopLevelVarDeclaredNames")
[989] StatementListItem[0,0].TopLevelVarDeclaredNames: Entry[26766]
[990] StatementListItem[0,0].TopLevelVarDeclaredNames: Normal[26767] let StatementListItem = this
[991] StatementListItem[0,0].TopLevelVarDeclaredNames: If[26770] (is-instance-of Statement Statement10)
[992] StatementListItem[0,0].TopLevelVarDeclaredNames: Call[26769] access __x1__ = (Statement "VarDeclaredNames")
[993] Statement[3,0].VarDeclaredNames: Entry[27134]
[994] Statement[3,0].VarDeclaredNames: Normal[27135] let Statement = this
[995] Statement[3,0].VarDeclaredNames: Normal[27136] return (new [])
<RETURN> #29 -> []
[996] StatementListItem[0,0].TopLevelVarDeclaredNames: Normal[26771] return __x1__
<RETURN> N(#29) -> []
[997] StatementList[1,0].TopLevelVarDeclaredNames: Normal[26954] let __x2__ = __x1__
[998] StatementList[1,0].TopLevelVarDeclaredNames: Normal[26945] let __x3__ = 0i
[999] StatementList[1,0].TopLevelVarDeclaredNames: Loop[26946] (< __x3__ __x2__.length)
[1000] StatementList[1,0].TopLevelVarDeclaredNames: Normal[26950] return names
<RETURN> N(#28) -> ["x"]
[1001] ScriptBody[0,0].VarDeclaredNames: Normal[26012] return __x0__
<RETURN> N(#28) -> ["x"]
[1002] GlobalDeclarationInstantiation: Normal[19615] let varNames = __x1__
[1003] GlobalDeclarationInstantiation: Normal[19616] let __x2__ = lexNames
[1004] GlobalDeclarationInstantiation: Normal[19657] let __x3__ = 0i
[1005] GlobalDeclarationInstantiation: Loop[19663] (< __x3__ __x2__.length)
[1006] GlobalDeclarationInstantiation: Normal[19690] let __x7__ = varNames
[1007] GlobalDeclarationInstantiation: Normal[19691] let __x8__ = 0i
[1008] GlobalDeclarationInstantiation: Loop[19623] (< __x8__ __x7__.length)
[1009] GlobalDeclarationInstantiation: Normal[19624] let name = __x7__[__x8__]
[1010] GlobalDeclarationInstantiation: Normal[19629] __x8__ = (+ __x8__ 1i)
[1011] GlobalDeclarationInstantiation: Call[19695] app __x9__ = (env.HasLexicalDeclaration env name)
[1012] GlobalEnvironmentRecord.HasLexicalDeclaration: Entry[19838]
[1013] GlobalEnvironmentRecord.HasLexicalDeclaration: Normal[19839] let DclRec = envRec.DeclarativeRecord
[1014] GlobalEnvironmentRecord.HasLexicalDeclaration: Call[19840] app __x0__ = (DclRec.HasBinding DclRec N)
[1015] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[1016] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[1017] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[1018] GlobalEnvironmentRecord.HasLexicalDeclaration: Normal[19841] return __x0__
<RETURN> N(false)
[1019] GlobalDeclarationInstantiation: If[19666] (= __x9__ true)
[1020] GlobalDeclarationInstantiation: LoopCont[19646]
[1021] GlobalDeclarationInstantiation: Loop[19623] (< __x8__ __x7__.length)
[1022] GlobalDeclarationInstantiation: Call[19625] access __x10__ = (script "VarScopedDeclarations")
[1023] ScriptBody[0,0].VarScopedDeclarations: Entry[26014]
[1024] ScriptBody[0,0].VarScopedDeclarations: Normal[26015] let ScriptBody = this
[1025] ScriptBody[0,0].VarScopedDeclarations: Call[26016] access __x0__ = (StatementList "TopLevelVarScopedDeclarations")
[1026] StatementList[1,0].TopLevelVarScopedDeclarations: Entry[26956]
[1027] StatementList[1,0].TopLevelVarScopedDeclarations: Call[26957] access __x0__ = (StatementList "TopLevelVarScopedDeclarations")
[1028] StatementListItem[0,0].TopLevelVarScopedDeclarations: Entry[26775]
[1029] StatementListItem[0,0].TopLevelVarScopedDeclarations: Normal[26776] let StatementListItem = this
[1030] StatementListItem[0,0].TopLevelVarScopedDeclarations: If[26779] (is-instance-of Statement Statement10)
[1031] StatementListItem[0,0].TopLevelVarScopedDeclarations: Call[26778] access __x1__ = (Statement "VarScopedDeclarations")
[1032] VariableDeclarationList[0,0].VarScopedDeclarations: Entry[29048]
[1033] VariableDeclarationList[0,0].VarScopedDeclarations: Normal[29049] let VariableDeclarationList = this
[1034] VariableDeclarationList[0,0].VarScopedDeclarations: Normal[29050] return (new [VariableDeclaration])
<RETURN> #30 -> [☊[VariableDeclaration](x = 1 + 2)]
[1035] StatementListItem[0,0].TopLevelVarScopedDeclarations: Normal[26780] return __x1__
<RETURN> N(#30) -> [☊[VariableDeclaration](x = 1 + 2)]
[1036] StatementList[1,0].TopLevelVarScopedDeclarations: Normal[26961] let declarations = __x0__
[1037] StatementList[1,0].TopLevelVarScopedDeclarations: Call[26965] access __x1__ = (StatementListItem "TopLevelVarScopedDeclarations")
[1038] StatementListItem[0,0].TopLevelVarScopedDeclarations: Entry[26775]
[1039] StatementListItem[0,0].TopLevelVarScopedDeclarations: Normal[26776] let StatementListItem = this
[1040] StatementListItem[0,0].TopLevelVarScopedDeclarations: If[26779] (is-instance-of Statement Statement10)
[1041] StatementListItem[0,0].TopLevelVarScopedDeclarations: Call[26778] access __x1__ = (Statement "VarScopedDeclarations")
[1042] Statement[3,0].VarScopedDeclarations: Entry[27138]
[1043] Statement[3,0].VarScopedDeclarations: Normal[27139] let Statement = this
[1044] Statement[3,0].VarScopedDeclarations: Normal[27140] return (new [])
<RETURN> #31 -> []
[1045] StatementListItem[0,0].TopLevelVarScopedDeclarations: Normal[26780] return __x1__
<RETURN> N(#31) -> []
[1046] StatementList[1,0].TopLevelVarScopedDeclarations: Normal[26967] let __x2__ = __x1__
[1047] StatementList[1,0].TopLevelVarScopedDeclarations: Normal[26958] let __x3__ = 0i
[1048] StatementList[1,0].TopLevelVarScopedDeclarations: Loop[26959] (< __x3__ __x2__.length)
[1049] StatementList[1,0].TopLevelVarScopedDeclarations: Normal[26963] return declarations
<RETURN> N(#30) -> [☊[VariableDeclaration](x = 1 + 2)]
[1050] ScriptBody[0,0].VarScopedDeclarations: Normal[26017] return __x0__
<RETURN> N(#30) -> [☊[VariableDeclaration](x = 1 + 2)]
[1051] GlobalDeclarationInstantiation: Normal[19688] let varDeclarations = __x10__
[1052] GlobalDeclarationInstantiation: Normal[19664] let functionsToInitialize = (new [])
[1053] GlobalDeclarationInstantiation: Normal[19665] let declaredFunctionNames = (new [])
[1054] GlobalDeclarationInstantiation: Normal[19689] let __x11__ = varDeclarations
[1055] GlobalDeclarationInstantiation: Normal[19711] let __x12__ = __x11__.length
[1056] GlobalDeclarationInstantiation: Loop[19626] (< 0i __x12__)
[1057] GlobalDeclarationInstantiation: Normal[19627] __x12__ = (- __x12__ 1i)
[1058] GlobalDeclarationInstantiation: Normal[19667] let d = __x11__[__x12__]
[1059] GlobalDeclarationInstantiation: If[19704] (! (|| (|| (is-instance-of d VariableDeclaration) (is-instance-of d ForBinding)) (is-instance-of d BindingIdentifier)))
[1060] GlobalDeclarationInstantiation: LoopCont[19693]
[1061] GlobalDeclarationInstantiation: Loop[19626] (< 0i __x12__)
[1062] GlobalDeclarationInstantiation: Normal[19628] let declaredVarNames = (new [])
[1063] GlobalDeclarationInstantiation: Normal[19630] let __x15__ = varDeclarations
[1064] GlobalDeclarationInstantiation: Normal[19674] let __x16__ = 0i
[1065] GlobalDeclarationInstantiation: Loop[19681] (< __x16__ __x15__.length)
[1066] GlobalDeclarationInstantiation: Normal[19619] let d = __x15__[__x16__]
[1067] GlobalDeclarationInstantiation: Normal[19620] __x16__ = (+ __x16__ 1i)
[1068] GlobalDeclarationInstantiation: If[19641] (|| (|| (is-instance-of d VariableDeclaration) (is-instance-of d ForBinding)) (is-instance-of d BindingIdentifier))
[1069] GlobalDeclarationInstantiation: Call[19694] access __x17__ = (d "BoundNames")
[1070] VariableDeclaration[0,1].BoundNames: Entry[29087]
[1071] VariableDeclaration[0,1].BoundNames: Normal[29088] let VariableDeclaration = this
[1072] VariableDeclaration[0,1].BoundNames: Call[29089] access __x0__ = (BindingIdentifier "BoundNames")
[1073] BindingIdentifier[0,0].BoundNames: Entry[3476]
[1074] BindingIdentifier[0,0].BoundNames: Normal[3477] let BindingIdentifier = this
[1075] BindingIdentifier[0,0].BoundNames: Call[3478] access __x0__ = (Identifier "StringValue")
[1076] Identifier[0,0].StringValue: Entry[20090]
[1077] Identifier[0,0].StringValue: Normal[20091] let Identifier = this
[1078] Identifier[0,0].StringValue: Call[20092] access __x0__ = (IdentifierName "StringValue")
[1079] Identifier[0,0].StringValue: Normal[20093] return __x0__
<RETURN> "x"
[1080] BindingIdentifier[0,0].BoundNames: Normal[3479] return (new [__x0__])
<RETURN> #35 -> ["x"]
[1081] VariableDeclaration[0,1].BoundNames: Normal[29090] return __x0__
<RETURN> N(#35) -> ["x"]
[1082] GlobalDeclarationInstantiation: Normal[19658] let __x18__ = __x17__
[1083] GlobalDeclarationInstantiation: Normal[19651] let __x19__ = 0i
[1084] GlobalDeclarationInstantiation: Loop[19652] (< __x19__ __x18__.length)
[1085] GlobalDeclarationInstantiation: Normal[19713] let vn = __x18__[__x19__]
[1086] GlobalDeclarationInstantiation: Normal[19685] __x19__ = (+ __x19__ 1i)
[1087] GlobalDeclarationInstantiation: If[19669] (! (contains declaredFunctionNames vn))
[1088] GlobalDeclarationInstantiation: Call[19670] app __x20__ = (env.CanDeclareGlobalVar env vn)
[1089] GlobalEnvironmentRecord.CanDeclareGlobalVar: Entry[19732]
[1090] GlobalEnvironmentRecord.CanDeclareGlobalVar: Normal[19733] let ObjRec = envRec.ObjectRecord
[1091] GlobalEnvironmentRecord.CanDeclareGlobalVar: Normal[19737] let globalObject = ObjRec.BindingObject
[1092] GlobalEnvironmentRecord.CanDeclareGlobalVar: Call[19738] app __x0__ = (HasOwnProperty globalObject N)
[1093] HasOwnProperty: Entry[19889]
[1094] HasOwnProperty: Normal[19890] assert (= (typeof O) Object)
[1095] HasOwnProperty: Call[19893] app __x0__ = (IsPropertyKey P)
[1096] IsPropertyKey: Entry[21126]
[1097] IsPropertyKey: If[21127] (= (typeof argument) String)
[1098] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1099] HasOwnProperty: Normal[19896] assert (= __x0__ true)
[1100] HasOwnProperty: Call[19897] app __x1__ = (O.GetOwnProperty O P)
[1101] OrdinaryObject.GetOwnProperty: Entry[23863]
[1102] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1103] OrdinaryGetOwnProperty: Entry[23788]
[1104] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1105] IsPropertyKey: Entry[21126]
[1106] IsPropertyKey: If[21127] (= (typeof argument) String)
[1107] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1108] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1109] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1110] OrdinaryGetOwnProperty: Normal[23804] return undefined
<RETURN> undefined
[1111] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> undefined
[1112] HasOwnProperty: Normal[19891] let desc = [? __x1__]
[1113] HasOwnProperty: If[19892] (= desc undefined)
[1114] HasOwnProperty: Normal[19894] return false
<RETURN> false
[1115] GlobalEnvironmentRecord.CanDeclareGlobalVar: Normal[19740] let hasProperty = [? __x0__]
[1116] GlobalEnvironmentRecord.CanDeclareGlobalVar: If[19734] (= hasProperty true)
[1117] GlobalEnvironmentRecord.CanDeclareGlobalVar: Call[19736] app __x1__ = (IsExtensible globalObject)
[1118] IsExtensible: Entry[21043]
[1119] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[1120] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[1121] OrdinaryObject.IsExtensible: Entry[23875]
[1122] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[1123] OrdinaryIsExtensible: Entry[23848]
[1124] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[1125] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[1126] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[1127] GlobalEnvironmentRecord.CanDeclareGlobalVar: Normal[19739] return [? __x1__]
<RETURN> true
[1128] GlobalDeclarationInstantiation: Normal[19707] let vnDefinable = [? __x20__]
[1129] GlobalDeclarationInstantiation: If[19715] (= vnDefinable false)
[1130] GlobalDeclarationInstantiation: If[19605] (! (contains declaredVarNames vn))
[1131] GlobalDeclarationInstantiation: Normal[19661] append vn -> declaredVarNames
[1132] GlobalDeclarationInstantiation: LoopCont[19662]
[1133] GlobalDeclarationInstantiation: Loop[19652] (< __x19__ __x18__.length)
[1134] GlobalDeclarationInstantiation: LoopCont[19680]
[1135] GlobalDeclarationInstantiation: Loop[19681] (< __x16__ __x15__.length)
[1136] GlobalDeclarationInstantiation: Call[19655] access __x21__ = (script "LexicallyScopedDeclarations")
[1137] ScriptBody[0,0].LexicallyScopedDeclarations: Entry[26004]
[1138] ScriptBody[0,0].LexicallyScopedDeclarations: Normal[26005] let ScriptBody = this
[1139] ScriptBody[0,0].LexicallyScopedDeclarations: Call[26006] access __x0__ = (StatementList "TopLevelLexicallyScopedDeclarations")
[1140] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Entry[26930]
[1141] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Call[26931] access __x0__ = (StatementList "TopLevelLexicallyScopedDeclarations")
[1142] StatementListItem[0,0].TopLevelLexicallyScopedDeclarations: Entry[26762]
[1143] StatementListItem[0,0].TopLevelLexicallyScopedDeclarations: Normal[26763] let StatementListItem = this
[1144] StatementListItem[0,0].TopLevelLexicallyScopedDeclarations: Normal[26764] return (new [])
<RETURN> #36 -> []
[1145] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Normal[26935] let declarations = __x0__
[1146] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Call[26939] access __x1__ = (StatementListItem "TopLevelLexicallyScopedDeclarations")
[1147] StatementListItem[0,0].TopLevelLexicallyScopedDeclarations: Entry[26762]
[1148] StatementListItem[0,0].TopLevelLexicallyScopedDeclarations: Normal[26763] let StatementListItem = this
[1149] StatementListItem[0,0].TopLevelLexicallyScopedDeclarations: Normal[26764] return (new [])
<RETURN> #37 -> []
[1150] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Normal[26941] let __x2__ = __x1__
[1151] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Normal[26932] let __x3__ = 0i
[1152] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Loop[26933] (< __x3__ __x2__.length)
[1153] StatementList[1,0].TopLevelLexicallyScopedDeclarations: Normal[26937] return declarations
<RETURN> N(#36) -> []
[1154] ScriptBody[0,0].LexicallyScopedDeclarations: Normal[26007] return __x0__
<RETURN> N(#36) -> []
[1155] GlobalDeclarationInstantiation: Normal[19656] let lexDeclarations = __x21__
[1156] GlobalDeclarationInstantiation: Normal[19703] let __x22__ = lexDeclarations
[1157] GlobalDeclarationInstantiation: Normal[19676] let __x23__ = 0i
[1158] GlobalDeclarationInstantiation: Loop[19642] (< __x23__ __x22__.length)
[1159] GlobalDeclarationInstantiation: Normal[19644] let __x30__ = functionsToInitialize
[1160] GlobalDeclarationInstantiation: Normal[19677] let __x31__ = 0i
[1161] GlobalDeclarationInstantiation: Loop[19648] (< __x31__ __x30__.length)
[1162] GlobalDeclarationInstantiation: Normal[19672] let __x35__ = declaredVarNames
[1163] GlobalDeclarationInstantiation: Normal[19708] let __x36__ = 0i
[1164] GlobalDeclarationInstantiation: Loop[19675] (< __x36__ __x35__.length)
[1165] GlobalDeclarationInstantiation: Normal[19633] let vn = __x35__[__x36__]
[1166] GlobalDeclarationInstantiation: Normal[19634] __x36__ = (+ __x36__ 1i)
[1167] GlobalDeclarationInstantiation: Call[19602] app __x37__ = (env.CreateGlobalVarBinding env vn false)
[1168] GlobalEnvironmentRecord.CreateGlobalVarBinding: Entry[19759]
[1169] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19760] let ObjRec = envRec.ObjectRecord
[1170] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19767] let globalObject = ObjRec.BindingObject
[1171] GlobalEnvironmentRecord.CreateGlobalVarBinding: Call[19771] app __x0__ = (HasOwnProperty globalObject N)
[1172] HasOwnProperty: Entry[19889]
[1173] HasOwnProperty: Normal[19890] assert (= (typeof O) Object)
[1174] HasOwnProperty: Call[19893] app __x0__ = (IsPropertyKey P)
[1175] IsPropertyKey: Entry[21126]
[1176] IsPropertyKey: If[21127] (= (typeof argument) String)
[1177] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1178] HasOwnProperty: Normal[19896] assert (= __x0__ true)
[1179] HasOwnProperty: Call[19897] app __x1__ = (O.GetOwnProperty O P)
[1180] OrdinaryObject.GetOwnProperty: Entry[23863]
[1181] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1182] OrdinaryGetOwnProperty: Entry[23788]
[1183] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1184] IsPropertyKey: Entry[21126]
[1185] IsPropertyKey: If[21127] (= (typeof argument) String)
[1186] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1187] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1188] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1189] OrdinaryGetOwnProperty: Normal[23804] return undefined
<RETURN> undefined
[1190] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> undefined
[1191] HasOwnProperty: Normal[19891] let desc = [? __x1__]
[1192] HasOwnProperty: If[19892] (= desc undefined)
[1193] HasOwnProperty: Normal[19894] return false
<RETURN> false
[1194] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19774] let hasProperty = [? __x0__]
[1195] GlobalEnvironmentRecord.CreateGlobalVarBinding: Call[19761] app __x1__ = (IsExtensible globalObject)
[1196] IsExtensible: Entry[21043]
[1197] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[1198] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[1199] OrdinaryObject.IsExtensible: Entry[23875]
[1200] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[1201] OrdinaryIsExtensible: Entry[23848]
[1202] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[1203] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[1204] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[1205] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19762] let extensible = [? __x1__]
[1206] GlobalEnvironmentRecord.CreateGlobalVarBinding: If[19768] (&& (= hasProperty false) (= extensible true))
[1207] GlobalEnvironmentRecord.CreateGlobalVarBinding: Call[19773] app __x2__ = (ObjRec.CreateMutableBinding ObjRec N D)
[1208] ObjectEnvironmentRecord.CreateMutableBinding: Entry[23452]
[1209] ObjectEnvironmentRecord.CreateMutableBinding: Normal[23453] let bindings = envRec.BindingObject
[1210] ObjectEnvironmentRecord.CreateMutableBinding: Call[23454] app __x0__ = (DefinePropertyOrThrow bindings N (new PropertyDescriptor("Value" -> undefined, "Writable" -> true, "Enumerable" -> true, "Configurable" -> D)))
[1211] DefinePropertyOrThrow: Entry[7579]
[1212] DefinePropertyOrThrow: Normal[7580] assert (= (typeof O) Object)
[1213] DefinePropertyOrThrow: Call[7583] app __x0__ = (IsPropertyKey P)
[1214] IsPropertyKey: Entry[21126]
[1215] IsPropertyKey: If[21127] (= (typeof argument) String)
[1216] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1217] DefinePropertyOrThrow: Normal[7586] assert (= __x0__ true)
[1218] DefinePropertyOrThrow: Call[7587] app __x1__ = (O.DefineOwnProperty O P desc)
[1219] OrdinaryObject.DefineOwnProperty: Entry[23851]
[1220] OrdinaryObject.DefineOwnProperty: Call[23852] app __x0__ = (OrdinaryDefineOwnProperty O P Desc)
[1221] OrdinaryDefineOwnProperty: Entry[23715]
[1222] OrdinaryDefineOwnProperty: Call[23716] app __x0__ = (O.GetOwnProperty O P)
[1223] OrdinaryObject.GetOwnProperty: Entry[23863]
[1224] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1225] OrdinaryGetOwnProperty: Entry[23788]
[1226] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1227] IsPropertyKey: Entry[21126]
[1228] IsPropertyKey: If[21127] (= (typeof argument) String)
[1229] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1230] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1231] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1232] OrdinaryGetOwnProperty: Normal[23804] return undefined
<RETURN> undefined
[1233] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> undefined
[1234] OrdinaryDefineOwnProperty: Normal[23719] let current = [? __x0__]
[1235] OrdinaryDefineOwnProperty: Call[23721] app __x1__ = (IsExtensible O)
[1236] IsExtensible: Entry[21043]
[1237] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[1238] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[1239] OrdinaryObject.IsExtensible: Entry[23875]
[1240] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[1241] OrdinaryIsExtensible: Entry[23848]
[1242] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[1243] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[1244] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[1245] OrdinaryDefineOwnProperty: Normal[23722] let extensible = [? __x1__]
[1246] OrdinaryDefineOwnProperty: Call[23717] app __x2__ = (ValidateAndApplyPropertyDescriptor O P extensible Desc current)
[1247] ValidateAndApplyPropertyDescriptor: Entry[28891]
[1248] ValidateAndApplyPropertyDescriptor: If[28892] (= current undefined)
[1249] ValidateAndApplyPropertyDescriptor: If[28937] (= extensible false)
[1250] ValidateAndApplyPropertyDescriptor: Normal[28965] assert (= extensible true)
[1251] ValidateAndApplyPropertyDescriptor: Normal[28883] let __x0__ = true
[1252] ValidateAndApplyPropertyDescriptor: Call[28884] app __x1__ = (IsGenericDescriptor Desc)
[1253] IsGenericDescriptor: Entry[21048]
[1254] IsGenericDescriptor: If[21049] (= Desc undefined)
[1255] IsGenericDescriptor: Call[21054] app __x0__ = (IsAccessorDescriptor Desc)
[1256] IsAccessorDescriptor: Entry[20967]
[1257] IsAccessorDescriptor: If[20968] (= Desc undefined)
[1258] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[1259] IsAccessorDescriptor: Normal[20973] return false
<RETURN> false
[1260] IsGenericDescriptor: Call[21056] app __x1__ = (IsDataDescriptor Desc)
[1261] IsDataDescriptor: Entry[21031]
[1262] IsDataDescriptor: If[21032] (= Desc undefined)
[1263] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1264] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1265] IsGenericDescriptor: If[21050] (&& (= __x0__ false) (= __x1__ false))
[1266] IsGenericDescriptor: Normal[21052] return false
<RETURN> false
[1267] ValidateAndApplyPropertyDescriptor: Normal[28941] __x0__ = (= __x1__ true)
[1268] ValidateAndApplyPropertyDescriptor: If[28982] __x0__
[1269] ValidateAndApplyPropertyDescriptor: Call[28956] app __x2__ = (IsDataDescriptor Desc)
[1270] IsDataDescriptor: Entry[21031]
[1271] IsDataDescriptor: If[21032] (= Desc undefined)
[1272] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1273] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1274] ValidateAndApplyPropertyDescriptor: Normal[28895] __x0__ = (= __x2__ true)
[1275] ValidateAndApplyPropertyDescriptor: If[28896] __x0__
[1276] ValidateAndApplyPropertyDescriptor: If[28976] (! (= O undefined))
[1277] ValidateAndApplyPropertyDescriptor: Normal[28960] let dp = (new DataProperty())
[1278] ValidateAndApplyPropertyDescriptor: If[28910] (! (= absent Desc.Value))
[1279] ValidateAndApplyPropertyDescriptor: Normal[28911] dp.Value = Desc.Value
[1280] ValidateAndApplyPropertyDescriptor: If[28967] (! (= absent Desc.Writable))
[1281] ValidateAndApplyPropertyDescriptor: Normal[28968] dp.Writable = Desc.Writable
[1282] ValidateAndApplyPropertyDescriptor: If[28915] (! (= absent Desc.Enumerable))
[1283] ValidateAndApplyPropertyDescriptor: Normal[28916] dp.Enumerable = Desc.Enumerable
[1284] ValidateAndApplyPropertyDescriptor: If[28946] (! (= absent Desc.Configurable))
[1285] ValidateAndApplyPropertyDescriptor: Normal[28901] dp.Configurable = Desc.Configurable
[1286] ValidateAndApplyPropertyDescriptor: Normal[28902] O.SubMap[P] = dp
[1287] ValidateAndApplyPropertyDescriptor: Normal[28928] return true
<RETURN> true
[1288] OrdinaryDefineOwnProperty: Normal[23718] return __x2__
<RETURN> N(true)
[1289] OrdinaryObject.DefineOwnProperty: Normal[23853] return [? __x0__]
<RETURN> true
[1290] DefinePropertyOrThrow: Normal[7581] let success = [? __x1__]
[1291] DefinePropertyOrThrow: If[7582] (= success false)
[1292] DefinePropertyOrThrow: Normal[7585] return success
<RETURN> true
[1293] ObjectEnvironmentRecord.CreateMutableBinding: Normal[23455] return [? __x0__]
<RETURN> true
[1294] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19769] [? __x2__]
[1295] GlobalEnvironmentRecord.CreateGlobalVarBinding: Call[19763] app __x3__ = (ObjRec.InitializeBinding ObjRec N undefined)
[1296] ObjectEnvironmentRecord.InitializeBinding: Entry[23497]
[1297] ObjectEnvironmentRecord.InitializeBinding: Call[23498] app __x0__ = (envRec.SetMutableBinding envRec N V false)
[1298] ObjectEnvironmentRecord.SetMutableBinding: Entry[23501]
[1299] ObjectEnvironmentRecord.SetMutableBinding: Normal[23502] let bindings = envRec.BindingObject
[1300] ObjectEnvironmentRecord.SetMutableBinding: Call[23505] app __x0__ = (HasProperty bindings N)
[1301] HasProperty: Entry[19899]
[1302] HasProperty: Normal[19900] assert (= (typeof O) Object)
[1303] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[1304] IsPropertyKey: Entry[21126]
[1305] IsPropertyKey: If[21127] (= (typeof argument) String)
[1306] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1307] HasProperty: Normal[19904] assert (= __x0__ true)
[1308] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[1309] OrdinaryObject.HasProperty: Entry[23871]
[1310] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[1311] OrdinaryHasProperty: Entry[23834]
[1312] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[1313] IsPropertyKey: Entry[21126]
[1314] IsPropertyKey: If[21127] (= (typeof argument) String)
[1315] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1316] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[1317] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[1318] OrdinaryObject.GetOwnProperty: Entry[23863]
[1319] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1320] OrdinaryGetOwnProperty: Entry[23788]
[1321] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1322] IsPropertyKey: Entry[21126]
[1323] IsPropertyKey: If[21127] (= (typeof argument) String)
[1324] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1325] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1326] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1327] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1328] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1329] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1330] IsDataDescriptor: Entry[21031]
[1331] IsDataDescriptor: If[21032] (= Desc undefined)
[1332] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1333] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1334] OrdinaryGetOwnProperty: If[23803] __x1__
[1335] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1336] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1337] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1338] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1339] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #40 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1340] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #40 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1341] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[1342] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[1343] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[1344] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[1345] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[1346] ObjectEnvironmentRecord.SetMutableBinding: Normal[23507] let stillExists = [? __x0__]
[1347] ObjectEnvironmentRecord.SetMutableBinding: If[23509] (&& (= stillExists false) (= S true))
[1348] ObjectEnvironmentRecord.SetMutableBinding: Call[23504] app __x1__ = (Set bindings N V S)
[1349] Set: Entry[26220]
[1350] Set: Normal[26221] assert (= (typeof O) Object)
[1351] Set: Call[26224] app __x0__ = (IsPropertyKey P)
[1352] IsPropertyKey: Entry[21126]
[1353] IsPropertyKey: If[21127] (= (typeof argument) String)
[1354] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1355] Set: Normal[26228] assert (= __x0__ true)
[1356] Set: Normal[26230] assert (= (typeof Throw) Boolean)
[1357] Set: Call[26222] app __x1__ = (O.Set O P V O)
[1358] OrdinaryObject.Set: Entry[23887]
[1359] OrdinaryObject.Set: Call[23888] app __x0__ = (OrdinarySet O P V Receiver)
[1360] OrdinarySet: Entry[23943]
[1361] OrdinarySet: Call[23944] app __x0__ = (IsPropertyKey P)
[1362] IsPropertyKey: Entry[21126]
[1363] IsPropertyKey: If[21127] (= (typeof argument) String)
[1364] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1365] OrdinarySet: Normal[23947] assert (= __x0__ true)
[1366] OrdinarySet: Call[23949] app __x1__ = (O.GetOwnProperty O P)
[1367] OrdinaryObject.GetOwnProperty: Entry[23863]
[1368] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1369] OrdinaryGetOwnProperty: Entry[23788]
[1370] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1371] IsPropertyKey: Entry[21126]
[1372] IsPropertyKey: If[21127] (= (typeof argument) String)
[1373] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1374] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1375] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1376] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1377] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1378] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1379] IsDataDescriptor: Entry[21031]
[1380] IsDataDescriptor: If[21032] (= Desc undefined)
[1381] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1382] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1383] OrdinaryGetOwnProperty: If[23803] __x1__
[1384] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1385] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1386] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1387] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1388] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #41 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1389] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #41 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1390] OrdinarySet: Normal[23950] let ownDesc = [? __x1__]
[1391] OrdinarySet: Call[23945] app __x2__ = (OrdinarySetWithOwnDescriptor O P V Receiver ownDesc)
[1392] OrdinarySetWithOwnDescriptor: Entry[23974]
[1393] OrdinarySetWithOwnDescriptor: Call[23975] app __x0__ = (IsPropertyKey P)
[1394] IsPropertyKey: Entry[21126]
[1395] IsPropertyKey: If[21127] (= (typeof argument) String)
[1396] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1397] OrdinarySetWithOwnDescriptor: Normal[23983] assert (= __x0__ true)
[1398] OrdinarySetWithOwnDescriptor: If[23987] (= ownDesc undefined)
[1399] OrdinarySetWithOwnDescriptor: Call[23978] app __x3__ = (IsDataDescriptor ownDesc)
[1400] IsDataDescriptor: Entry[21031]
[1401] IsDataDescriptor: If[21032] (= Desc undefined)
[1402] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1403] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1404] OrdinarySetWithOwnDescriptor: If[23979] (= __x3__ true)
[1405] OrdinarySetWithOwnDescriptor: If[23988] (= ownDesc.Writable false)
[1406] OrdinarySetWithOwnDescriptor: If[23980] (! (= (typeof Receiver) Object))
[1407] OrdinarySetWithOwnDescriptor: Call[23982] app __x4__ = (Receiver.GetOwnProperty Receiver P)
[1408] OrdinaryObject.GetOwnProperty: Entry[23863]
[1409] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1410] OrdinaryGetOwnProperty: Entry[23788]
[1411] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1412] IsPropertyKey: Entry[21126]
[1413] IsPropertyKey: If[21127] (= (typeof argument) String)
[1414] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1415] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1416] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1417] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1418] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1419] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1420] IsDataDescriptor: Entry[21031]
[1421] IsDataDescriptor: If[21032] (= Desc undefined)
[1422] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1423] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1424] OrdinaryGetOwnProperty: If[23803] __x1__
[1425] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1426] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1427] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1428] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1429] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #42 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1430] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #42 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1431] OrdinarySetWithOwnDescriptor: Normal[24005] let existingDescriptor = [? __x4__]
[1432] OrdinarySetWithOwnDescriptor: If[23990] (! (= existingDescriptor undefined))
[1433] OrdinarySetWithOwnDescriptor: Call[23991] app __x5__ = (IsAccessorDescriptor existingDescriptor)
[1434] IsAccessorDescriptor: Entry[20967]
[1435] IsAccessorDescriptor: If[20968] (= Desc undefined)
[1436] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[1437] IsAccessorDescriptor: Normal[20973] return false
<RETURN> false
[1438] OrdinarySetWithOwnDescriptor: If[23998] (= __x5__ true)
[1439] OrdinarySetWithOwnDescriptor: If[24000] (= existingDescriptor.Writable false)
[1440] OrdinarySetWithOwnDescriptor: Normal[23995] let valueDesc = (new PropertyDescriptor("Value" -> V))
[1441] OrdinarySetWithOwnDescriptor: Call[23996] app __x6__ = (Receiver.DefineOwnProperty Receiver P valueDesc)
[1442] OrdinaryObject.DefineOwnProperty: Entry[23851]
[1443] OrdinaryObject.DefineOwnProperty: Call[23852] app __x0__ = (OrdinaryDefineOwnProperty O P Desc)
[1444] OrdinaryDefineOwnProperty: Entry[23715]
[1445] OrdinaryDefineOwnProperty: Call[23716] app __x0__ = (O.GetOwnProperty O P)
[1446] OrdinaryObject.GetOwnProperty: Entry[23863]
[1447] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1448] OrdinaryGetOwnProperty: Entry[23788]
[1449] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1450] IsPropertyKey: Entry[21126]
[1451] IsPropertyKey: If[21127] (= (typeof argument) String)
[1452] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1453] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1454] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1455] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1456] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1457] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1458] IsDataDescriptor: Entry[21031]
[1459] IsDataDescriptor: If[21032] (= Desc undefined)
[1460] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1461] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1462] OrdinaryGetOwnProperty: If[23803] __x1__
[1463] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1464] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1465] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1466] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1467] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #44 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1468] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #44 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1469] OrdinaryDefineOwnProperty: Normal[23719] let current = [? __x0__]
[1470] OrdinaryDefineOwnProperty: Call[23721] app __x1__ = (IsExtensible O)
[1471] IsExtensible: Entry[21043]
[1472] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[1473] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[1474] OrdinaryObject.IsExtensible: Entry[23875]
[1475] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[1476] OrdinaryIsExtensible: Entry[23848]
[1477] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[1478] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[1479] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[1480] OrdinaryDefineOwnProperty: Normal[23722] let extensible = [? __x1__]
[1481] OrdinaryDefineOwnProperty: Call[23717] app __x2__ = (ValidateAndApplyPropertyDescriptor O P extensible Desc current)
[1482] ValidateAndApplyPropertyDescriptor: Entry[28891]
[1483] ValidateAndApplyPropertyDescriptor: If[28892] (= current undefined)
[1484] ValidateAndApplyPropertyDescriptor: If[28938] (&& (= absent Desc.Value) (&& (= absent Desc.Writable) (&& (= absent Desc.Get) (&& (= absent Desc.Set) (&& (= absent Desc.Enumerable) (= absent Desc.Configurable))))))
[1485] ValidateAndApplyPropertyDescriptor: If[28919] (= current.Configurable false)
[1486] ValidateAndApplyPropertyDescriptor: If[28989] (= Desc.Configurable true)
[1487] ValidateAndApplyPropertyDescriptor: Normal[28978] let __x4__ = true
[1488] ValidateAndApplyPropertyDescriptor: Normal[28992] __x4__ = (! (= Desc.Enumerable absent))
[1489] ValidateAndApplyPropertyDescriptor: If[28907] __x4__
[1490] ValidateAndApplyPropertyDescriptor: If[28909] __x4__
[1491] ValidateAndApplyPropertyDescriptor: Call[28898] app __x6__ = (IsGenericDescriptor Desc)
[1492] IsGenericDescriptor: Entry[21048]
[1493] IsGenericDescriptor: If[21049] (= Desc undefined)
[1494] IsGenericDescriptor: Call[21054] app __x0__ = (IsAccessorDescriptor Desc)
[1495] IsAccessorDescriptor: Entry[20967]
[1496] IsAccessorDescriptor: If[20968] (= Desc undefined)
[1497] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[1498] IsAccessorDescriptor: Normal[20973] return false
<RETURN> false
[1499] IsGenericDescriptor: Call[21056] app __x1__ = (IsDataDescriptor Desc)
[1500] IsDataDescriptor: Entry[21031]
[1501] IsDataDescriptor: If[21032] (= Desc undefined)
[1502] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1503] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1504] IsGenericDescriptor: If[21050] (&& (= __x0__ false) (= __x1__ false))
[1505] IsGenericDescriptor: Normal[21052] return false
<RETURN> false
[1506] ValidateAndApplyPropertyDescriptor: If[28923] (= [! __x6__] true)
[1507] ValidateAndApplyPropertyDescriptor: Call[28973] app __x7__ = (IsDataDescriptor current)
[1508] IsDataDescriptor: Entry[21031]
[1509] IsDataDescriptor: If[21032] (= Desc undefined)
[1510] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1511] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1512] ValidateAndApplyPropertyDescriptor: Call[28942] app __x8__ = (IsDataDescriptor Desc)
[1513] IsDataDescriptor: Entry[21031]
[1514] IsDataDescriptor: If[21032] (= Desc undefined)
[1515] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1516] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1517] ValidateAndApplyPropertyDescriptor: Call[28934] app __x9__ = (SameValue [! __x7__] [! __x8__])
[1518] SameValue: Entry[25946]
[1519] SameValue: If[25947] (! (= (typeof x) (typeof y)))
[1520] SameValue: If[25951] (|| (= (typeof x) Number) (= (typeof x) BigInt))
[1521] SameValue: Call[25949] app __x1__ = (SameValueNonNumeric x y)
[1522] SameValueNonNumeric: Entry[25955]
[1523] SameValueNonNumeric: Normal[25956] assert (! (|| (= (typeof x) Number) (= (typeof x) BigInt)))
[1524] SameValueNonNumeric: Normal[25966] assert (= (typeof x) (typeof y))
[1525] SameValueNonNumeric: If[25970] (= (typeof x) Undefined)
[1526] SameValueNonNumeric: If[25957] (= (typeof x) Null)
[1527] SameValueNonNumeric: If[25959] (= (typeof x) String)
[1528] SameValueNonNumeric: If[25967] (= (typeof x) Boolean)
[1529] SameValueNonNumeric: If[25960] (|| (&& (= x true) (= y true)) (&& (= x false) (= y false)))
[1530] SameValueNonNumeric: Normal[25961] return true
<RETURN> true
[1531] SameValue: Normal[25952] return [! __x1__]
<RETURN> true
[1532] ValidateAndApplyPropertyDescriptor: If[28935] (= [! __x9__] false)
[1533] ValidateAndApplyPropertyDescriptor: Call[28962] app __x11__ = (IsDataDescriptor current)
[1534] IsDataDescriptor: Entry[21031]
[1535] IsDataDescriptor: If[21032] (= Desc undefined)
[1536] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1537] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1538] ValidateAndApplyPropertyDescriptor: Call[28939] app __x12__ = (IsDataDescriptor Desc)
[1539] IsDataDescriptor: Entry[21031]
[1540] IsDataDescriptor: If[21032] (= Desc undefined)
[1541] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1542] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1543] ValidateAndApplyPropertyDescriptor: If[28940] (&& (= __x11__ true) (= __x12__ true))
[1544] ValidateAndApplyPropertyDescriptor: If[28981] (&& (= current.Configurable false) (= current.Writable false))
[1545] ValidateAndApplyPropertyDescriptor: If[28888] (! (= O undefined))
[1546] ValidateAndApplyPropertyDescriptor: Normal[28929] let __keys__ = (map-keys Desc)
[1547] ValidateAndApplyPropertyDescriptor: Normal[28987] let __i__ = 0i
[1548] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[1549] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[1550] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[1551] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[1552] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[1553] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[1554] ValidateAndApplyPropertyDescriptor: Normal[28930] return true
<RETURN> true
[1555] OrdinaryDefineOwnProperty: Normal[23718] return __x2__
<RETURN> N(true)
[1556] OrdinaryObject.DefineOwnProperty: Normal[23853] return [? __x0__]
<RETURN> true
[1557] OrdinarySetWithOwnDescriptor: Normal[23997] return [? __x6__]
<RETURN> true
[1558] OrdinarySet: Normal[23946] return __x2__
<RETURN> N(true)
[1559] OrdinaryObject.Set: Normal[23889] return [? __x0__]
<RETURN> true
[1560] Set: Normal[26223] let success = [? __x1__]
[1561] Set: If[26225] (&& (= success false) (= Throw true))
[1562] Set: Normal[26226] return success
<RETURN> true
[1563] ObjectEnvironmentRecord.SetMutableBinding: Normal[23506] return [? __x1__]
<RETURN> true
[1564] ObjectEnvironmentRecord.InitializeBinding: Normal[23499] return [? __x0__]
<RETURN> true
[1565] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19764] [? __x3__]
[1566] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19772] let varDeclaredNames = envRec.VarNames
[1567] GlobalEnvironmentRecord.CreateGlobalVarBinding: If[19770] (! (contains varDeclaredNames N))
[1568] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19765] append N -> varDeclaredNames
[1569] GlobalEnvironmentRecord.CreateGlobalVarBinding: Normal[19766] return ~empty~
<RETURN> ~empty~
[1570] GlobalDeclarationInstantiation: Normal[19603] [? __x37__]
[1571] GlobalDeclarationInstantiation: LoopCont[19700]
[1572] GlobalDeclarationInstantiation: Loop[19675] (< __x36__ __x35__.length)
[1573] GlobalDeclarationInstantiation: Normal[19613] return ~empty~
<RETURN> ~empty~
[1574] ScriptEvaluation: Normal[26035] let result = __x0__
[1575] ScriptEvaluation: If[26025] (= result.Type ~normal~)
[1576] ScriptEvaluation: Call[26026] access __x1__ = (scriptBody "Evaluation")
[1577] StatementList[1,0].Evaluation: Entry[26874]
[1578] StatementList[1,0].Evaluation: Call[26875] access __x0__ = (StatementList "Evaluation")
[1579] VariableStatement[0,0].Evaluation: Entry[29123]
[1580] VariableStatement[0,0].Evaluation: Normal[29124] let VariableStatement = this
[1581] VariableStatement[0,0].Evaluation: Call[29127] access __x0__ = (VariableDeclarationList "Evaluation")
[1582] VariableDeclaration[0,1].Evaluation: Entry[29092]
[1583] VariableDeclaration[0,1].Evaluation: Normal[29093] let VariableDeclaration = this
[1584] VariableDeclaration[0,1].Evaluation: Call[29100] access __x0__ = (BindingIdentifier "StringValue")
[1585] Identifier[0,0].StringValue: Entry[20090]
[1586] Identifier[0,0].StringValue: Normal[20091] let Identifier = this
[1587] Identifier[0,0].StringValue: Call[20092] access __x0__ = (IdentifierName "StringValue")
[1588] Identifier[0,0].StringValue: Normal[20093] return __x0__
<RETURN> "x"
[1589] VariableDeclaration[0,1].Evaluation: Normal[29104] let bindingId = __x0__
[1590] VariableDeclaration[0,1].Evaluation: Call[29107] app __x1__ = (ResolveBinding bindingId)
[1591] ResolveBinding: Entry[25799]
[1592] ResolveBinding: If[25800] (|| (= env absent) (= env undefined))
[1593] ResolveBinding: Normal[25803] env = CONTEXT.LexicalEnvironment
[1594] ResolveBinding: Normal[25804] assert (is-instance-of env EnvironmentRecord)
[1595] ResolveBinding: If[25807] true
[1596] ResolveBinding: Normal[25801] let strict = true
[1597] ResolveBinding: Call[25802] app __x0__ = (GetIdentifierReference env name strict)
[1598] GetIdentifierReference: Entry[19317]
[1599] GetIdentifierReference: If[19318] (= env null)
[1600] GetIdentifierReference: Call[19323] app __x0__ = (env.HasBinding env name)
[1601] GlobalEnvironmentRecord.HasBinding: Entry[19829]
[1602] GlobalEnvironmentRecord.HasBinding: Normal[19830] let DclRec = envRec.DeclarativeRecord
[1603] GlobalEnvironmentRecord.HasBinding: Call[19833] app __x0__ = (DclRec.HasBinding DclRec N)
[1604] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[1605] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[1606] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[1607] GlobalEnvironmentRecord.HasBinding: If[19835] (= __x0__ true)
[1608] GlobalEnvironmentRecord.HasBinding: Normal[19831] let ObjRec = envRec.ObjectRecord
[1609] GlobalEnvironmentRecord.HasBinding: Call[19832] app __x1__ = (ObjRec.HasBinding ObjRec N)
[1610] ObjectEnvironmentRecord.HasBinding: Entry[23473]
[1611] ObjectEnvironmentRecord.HasBinding: Normal[23474] let bindings = envRec.BindingObject
[1612] ObjectEnvironmentRecord.HasBinding: Call[23482] app __x0__ = (HasProperty bindings N)
[1613] HasProperty: Entry[19899]
[1614] HasProperty: Normal[19900] assert (= (typeof O) Object)
[1615] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[1616] IsPropertyKey: Entry[21126]
[1617] IsPropertyKey: If[21127] (= (typeof argument) String)
[1618] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1619] HasProperty: Normal[19904] assert (= __x0__ true)
[1620] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[1621] OrdinaryObject.HasProperty: Entry[23871]
[1622] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[1623] OrdinaryHasProperty: Entry[23834]
[1624] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[1625] IsPropertyKey: Entry[21126]
[1626] IsPropertyKey: If[21127] (= (typeof argument) String)
[1627] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1628] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[1629] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[1630] OrdinaryObject.GetOwnProperty: Entry[23863]
[1631] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1632] OrdinaryGetOwnProperty: Entry[23788]
[1633] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1634] IsPropertyKey: Entry[21126]
[1635] IsPropertyKey: If[21127] (= (typeof argument) String)
[1636] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1637] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1638] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1639] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1640] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1641] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1642] IsDataDescriptor: Entry[21031]
[1643] IsDataDescriptor: If[21032] (= Desc undefined)
[1644] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1645] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1646] OrdinaryGetOwnProperty: If[23803] __x1__
[1647] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1648] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1649] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1650] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1651] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #46 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1652] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #46 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1653] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[1654] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[1655] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[1656] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[1657] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[1658] ObjectEnvironmentRecord.HasBinding: Normal[23487] let foundBinding = [? __x0__]
[1659] ObjectEnvironmentRecord.HasBinding: If[23489] (= foundBinding false)
[1660] ObjectEnvironmentRecord.HasBinding: If[23476] (= envRec.withEnvironment false)
[1661] ObjectEnvironmentRecord.HasBinding: Normal[23483] return true
<RETURN> true
[1662] GlobalEnvironmentRecord.HasBinding: Normal[19834] return [? __x1__]
<RETURN> true
[1663] GetIdentifierReference: Normal[19327] let exists = [? __x0__]
[1664] GetIdentifierReference: If[19319] (= exists true)
[1665] GetIdentifierReference: Normal[19320] return (new ReferenceRecord("Base" -> env, "ReferencedName" -> name, "Strict" -> strict, "ThisValue" -> ~empty~))
<RETURN> #47 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("x")
}
[1666] ResolveBinding: Normal[25806] return [? __x0__]
<RETURN> #47 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("x")
}
[1667] VariableDeclaration[0,1].Evaluation: Normal[29094] let lhs = [? __x1__]
[1668] VariableDeclaration[0,1].Evaluation: Call[29095] app __x2__ = (IsAnonymousFunctionDefinition Initializer)
[1669] IsAnonymousFunctionDefinition: Entry[20974]
[1670] IsAnonymousFunctionDefinition: Call[20975] access __x0__ = (expr "IsFunctionDefinition")
[1671] AdditiveExpression[1,0].IsFunctionDefinition: Entry[196]
[1672] AdditiveExpression[1,0].IsFunctionDefinition: Normal[197] return false
<RETURN> false
[1673] IsAnonymousFunctionDefinition: If[20978] (= __x0__ false)
[1674] IsAnonymousFunctionDefinition: Normal[20981] return false
<RETURN> false
[1675] VariableDeclaration[0,1].Evaluation: If[29101] (= __x2__ true)
[1676] VariableDeclaration[0,1].Evaluation: Call[29096] access __x4__ = (Initializer "Evaluation")
[1677] AdditiveExpression[1,0].Evaluation: Entry[189]
[1678] AdditiveExpression[1,0].Evaluation: Call[190] app __x0__ = (EvaluateStringOrNumericBinaryExpression AdditiveExpression "+" MultiplicativeExpression)
[1679] EvaluateStringOrNumericBinaryExpression: Entry[8271]
[1680] EvaluateStringOrNumericBinaryExpression: Call[8272] access __x0__ = (leftOperand "Evaluation")
[1681] Literal[2,0].Evaluation: Entry[21728]
[1682] Literal[2,0].Evaluation: Normal[21729] let Literal = this
[1683] Literal[2,0].Evaluation: Call[21730] access __x0__ = (NumericLiteral "NumericValue")
[1684] Literal[2,0].Evaluation: Normal[21731] return __x0__
<RETURN> 1.0
[1685] EvaluateStringOrNumericBinaryExpression: Normal[8277] let lref = __x0__
[1686] EvaluateStringOrNumericBinaryExpression: Call[8280] app __x1__ = (GetValue lref)
[1687] GetValue: Entry[19545]
[1688] GetValue: Normal[19546] [? V]
[1689] GetValue: If[19554] (! (is-instance-of V ReferenceRecord))
[1690] GetValue: Normal[19558] return V
<RETURN> 1.0
[1691] EvaluateStringOrNumericBinaryExpression: Normal[8282] let lval = [? __x1__]
[1692] EvaluateStringOrNumericBinaryExpression: Call[8273] access __x2__ = (rightOperand "Evaluation")
[1693] Literal[2,0].Evaluation: Entry[21728]
[1694] Literal[2,0].Evaluation: Normal[21729] let Literal = this
[1695] Literal[2,0].Evaluation: Call[21730] access __x0__ = (NumericLiteral "NumericValue")
[1696] Literal[2,0].Evaluation: Normal[21731] return __x0__
<RETURN> 2.0
[1697] EvaluateStringOrNumericBinaryExpression: Normal[8274] let rref = __x2__
[1698] EvaluateStringOrNumericBinaryExpression: Call[8278] app __x3__ = (GetValue rref)
[1699] GetValue: Entry[19545]
[1700] GetValue: Normal[19546] [? V]
[1701] GetValue: If[19554] (! (is-instance-of V ReferenceRecord))
[1702] GetValue: Normal[19558] return V
<RETURN> 2.0
[1703] EvaluateStringOrNumericBinaryExpression: Normal[8281] let rval = [? __x3__]
[1704] EvaluateStringOrNumericBinaryExpression: Call[8279] app __x4__ = (ApplyStringOrNumericBinaryOperator lval opText rval)
[1705] ApplyStringOrNumericBinaryOperator: Entry[294]
[1706] ApplyStringOrNumericBinaryOperator: If[295] (= opText "+")
[1707] ApplyStringOrNumericBinaryOperator: Call[302] app __x0__ = (ToPrimitive lval)
[1708] ToPrimitive: Entry[28037]
[1709] ToPrimitive: If[28038] (= (typeof input) Object)
[1710] ToPrimitive: Normal[28046] return input
<RETURN> 1.0
[1711] ApplyStringOrNumericBinaryOperator: Normal[306] let lprim = [? __x0__]
[1712] ApplyStringOrNumericBinaryOperator: Call[309] app __x1__ = (ToPrimitive rval)
[1713] ToPrimitive: Entry[28037]
[1714] ToPrimitive: If[28038] (= (typeof input) Object)
[1715] ToPrimitive: Normal[28046] return input
<RETURN> 2.0
[1716] ApplyStringOrNumericBinaryOperator: Normal[296] let rprim = [? __x1__]
[1717] ApplyStringOrNumericBinaryOperator: If[297] (|| (= (typeof lprim) String) (= (typeof rprim) String))
[1718] ApplyStringOrNumericBinaryOperator: Normal[304] lval = lprim
[1719] ApplyStringOrNumericBinaryOperator: Normal[307] rval = rprim
[1720] ApplyStringOrNumericBinaryOperator: Call[300] app __x4__ = (ToNumeric lval)
[1721] ToNumeric: Entry[28004]
[1722] ToNumeric: Call[28005] app __x0__ = (ToPrimitive value ~number~)
[1723] ToPrimitive: Entry[28037]
[1724] ToPrimitive: If[28038] (= (typeof input) Object)
[1725] ToPrimitive: Normal[28046] return input
<RETURN> 1.0
[1726] ToNumeric: Normal[28008] let primValue = [? __x0__]
[1727] ToNumeric: If[28010] (= (typeof primValue) BigInt)
[1728] ToNumeric: Call[28006] app __x1__ = (ToNumber primValue)
[1729] ToNumber: Entry[27982]
[1730] ToNumber: If[27983] (= (typeof argument) Undefined)
[1731] ToNumber: If[27992] (= (typeof argument) Null)
[1732] ToNumber: If[27984] (= (typeof argument) Boolean)
[1733] ToNumber: If[27986] (= (typeof argument) Number)
[1734] ToNumber: Normal[27987] return argument
<RETURN> 1.0
[1735] ToNumeric: Normal[28007] return [? __x1__]
<RETURN> 1.0
[1736] ApplyStringOrNumericBinaryOperator: Normal[301] let lnum = [? __x4__]
[1737] ApplyStringOrNumericBinaryOperator: Call[342] app __x5__ = (ToNumeric rval)
[1738] ToNumeric: Entry[28004]
[1739] ToNumeric: Call[28005] app __x0__ = (ToPrimitive value ~number~)
[1740] ToPrimitive: Entry[28037]
[1741] ToPrimitive: If[28038] (= (typeof input) Object)
[1742] ToPrimitive: Normal[28046] return input
<RETURN> 2.0
[1743] ToNumeric: Normal[28008] let primValue = [? __x0__]
[1744] ToNumeric: If[28010] (= (typeof primValue) BigInt)
[1745] ToNumeric: Call[28006] app __x1__ = (ToNumber primValue)
[1746] ToNumber: Entry[27982]
[1747] ToNumber: If[27983] (= (typeof argument) Undefined)
[1748] ToNumber: If[27992] (= (typeof argument) Null)
[1749] ToNumber: If[27984] (= (typeof argument) Boolean)
[1750] ToNumber: If[27986] (= (typeof argument) Number)
[1751] ToNumber: Normal[27987] return argument
<RETURN> 2.0
[1752] ToNumeric: Normal[28007] return [? __x1__]
<RETURN> 2.0
[1753] ApplyStringOrNumericBinaryOperator: Normal[331] let rnum = [? __x5__]
[1754] ApplyStringOrNumericBinaryOperator: If[332] (! (= (typeof lnum) (typeof rnum)))
[1755] ApplyStringOrNumericBinaryOperator: Normal[318] let T = (typeof lnum)
[1756] ApplyStringOrNumericBinaryOperator: Normal[319] let m = PRIMITIVE[T]
[1757] ApplyStringOrNumericBinaryOperator: If[322] (= opText "**")
[1758] ApplyStringOrNumericBinaryOperator: If[313] (= opText "*")
[1759] ApplyStringOrNumericBinaryOperator: If[315] (= opText "/")
[1760] ApplyStringOrNumericBinaryOperator: If[324] (= opText "%")
[1761] ApplyStringOrNumericBinaryOperator: If[325] (= opText "+")
[1762] ApplyStringOrNumericBinaryOperator: Normal[343] let operation = m.add
[1763] ApplyStringOrNumericBinaryOperator: Call[317] app __x6__ = (operation lnum rnum)
[1764] Number::add: Entry[23143]
[1765] Number::add: Normal[23144] return (+ x y)
<RETURN> 3.0
[1766] ApplyStringOrNumericBinaryOperator: Normal[339] return [? __x6__]
<RETURN> 3.0
[1767] EvaluateStringOrNumericBinaryExpression: Normal[8275] return [? __x4__]
<RETURN> 3.0
[1768] AdditiveExpression[1,0].Evaluation: Normal[191] return [? __x0__]
<RETURN> 3.0
[1769] VariableDeclaration[0,1].Evaluation: Normal[29097] let rhs = __x4__
[1770] VariableDeclaration[0,1].Evaluation: Call[29105] app __x5__ = (GetValue rhs)
[1771] GetValue: Entry[19545]
[1772] GetValue: Normal[19546] [? V]
[1773] GetValue: If[19554] (! (is-instance-of V ReferenceRecord))
[1774] GetValue: Normal[19558] return V
<RETURN> 3.0
[1775] VariableDeclaration[0,1].Evaluation: Normal[29103] let value = [? __x5__]
[1776] VariableDeclaration[0,1].Evaluation: Call[29098] app __x6__ = (PutValue lhs value)
[1777] PutValue: Entry[25258]
[1778] PutValue: Normal[25259] [? V]
[1779] PutValue: Normal[25270] [? W]
[1780] PutValue: If[25274] (! (is-instance-of V ReferenceRecord))
[1781] PutValue: Call[25260] app __x0__ = (IsUnresolvableReference V)
[1782] IsUnresolvableReference: Entry[21178]
[1783] IsUnresolvableReference: Normal[21179] assert (is-instance-of V ReferenceRecord)
[1784] IsUnresolvableReference: If[21180] (= V.Base ~unresolvable~)
[1785] IsUnresolvableReference: Normal[21182] return false
<RETURN> false
[1786] PutValue: If[25261] (= __x0__ true)
[1787] PutValue: Call[25272] app __x3__ = (IsPropertyReference V)
[1788] IsPropertyReference: Entry[21133]
[1789] IsPropertyReference: Normal[21134] assert (is-instance-of V ReferenceRecord)
[1790] IsPropertyReference: If[21137] (= V.Base ~unresolvable~)
[1791] IsPropertyReference: If[21140] (|| (|| (|| (|| (|| (= (typeof V.Base) Boolean) (= (typeof V.Base) String)) (= (typeof V.Base) Symbol)) (= (typeof V.Base) BigInt)) (= (typeof V.Base) Number)) (= (typeof V.Base) Object))
[1792] IsPropertyReference: Normal[21138] return false
<RETURN> false
[1793] PutValue: If[25264] (= __x3__ true)
[1794] PutValue: Normal[25266] let base = V.Base
[1795] PutValue: Normal[25283] assert (is-instance-of base EnvironmentRecord)
[1796] PutValue: Call[25284] app __x7__ = (base.SetMutableBinding base V.ReferencedName W V.Strict)
[1797] GlobalEnvironmentRecord.SetMutableBinding: Entry[19876]
[1798] GlobalEnvironmentRecord.SetMutableBinding: Normal[19877] let DclRec = envRec.DeclarativeRecord
[1799] GlobalEnvironmentRecord.SetMutableBinding: Call[19880] app __x0__ = (DclRec.HasBinding DclRec N)
[1800] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[1801] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[1802] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[1803] GlobalEnvironmentRecord.SetMutableBinding: If[19882] (= __x0__ true)
[1804] GlobalEnvironmentRecord.SetMutableBinding: Normal[19879] let ObjRec = envRec.ObjectRecord
[1805] GlobalEnvironmentRecord.SetMutableBinding: Call[19881] app __x2__ = (ObjRec.SetMutableBinding ObjRec N V S)
[1806] ObjectEnvironmentRecord.SetMutableBinding: Entry[23501]
[1807] ObjectEnvironmentRecord.SetMutableBinding: Normal[23502] let bindings = envRec.BindingObject
[1808] ObjectEnvironmentRecord.SetMutableBinding: Call[23505] app __x0__ = (HasProperty bindings N)
[1809] HasProperty: Entry[19899]
[1810] HasProperty: Normal[19900] assert (= (typeof O) Object)
[1811] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[1812] IsPropertyKey: Entry[21126]
[1813] IsPropertyKey: If[21127] (= (typeof argument) String)
[1814] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1815] HasProperty: Normal[19904] assert (= __x0__ true)
[1816] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[1817] OrdinaryObject.HasProperty: Entry[23871]
[1818] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[1819] OrdinaryHasProperty: Entry[23834]
[1820] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[1821] IsPropertyKey: Entry[21126]
[1822] IsPropertyKey: If[21127] (= (typeof argument) String)
[1823] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1824] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[1825] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[1826] OrdinaryObject.GetOwnProperty: Entry[23863]
[1827] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1828] OrdinaryGetOwnProperty: Entry[23788]
[1829] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1830] IsPropertyKey: Entry[21126]
[1831] IsPropertyKey: If[21127] (= (typeof argument) String)
[1832] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1833] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1834] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1835] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1836] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1837] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1838] IsDataDescriptor: Entry[21031]
[1839] IsDataDescriptor: If[21032] (= Desc undefined)
[1840] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1841] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1842] OrdinaryGetOwnProperty: If[23803] __x1__
[1843] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1844] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1845] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1846] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1847] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #48 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1848] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #48 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1849] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[1850] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[1851] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[1852] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[1853] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[1854] ObjectEnvironmentRecord.SetMutableBinding: Normal[23507] let stillExists = [? __x0__]
[1855] ObjectEnvironmentRecord.SetMutableBinding: If[23509] (&& (= stillExists false) (= S true))
[1856] ObjectEnvironmentRecord.SetMutableBinding: Call[23504] app __x1__ = (Set bindings N V S)
[1857] Set: Entry[26220]
[1858] Set: Normal[26221] assert (= (typeof O) Object)
[1859] Set: Call[26224] app __x0__ = (IsPropertyKey P)
[1860] IsPropertyKey: Entry[21126]
[1861] IsPropertyKey: If[21127] (= (typeof argument) String)
[1862] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1863] Set: Normal[26228] assert (= __x0__ true)
[1864] Set: Normal[26230] assert (= (typeof Throw) Boolean)
[1865] Set: Call[26222] app __x1__ = (O.Set O P V O)
[1866] OrdinaryObject.Set: Entry[23887]
[1867] OrdinaryObject.Set: Call[23888] app __x0__ = (OrdinarySet O P V Receiver)
[1868] OrdinarySet: Entry[23943]
[1869] OrdinarySet: Call[23944] app __x0__ = (IsPropertyKey P)
[1870] IsPropertyKey: Entry[21126]
[1871] IsPropertyKey: If[21127] (= (typeof argument) String)
[1872] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1873] OrdinarySet: Normal[23947] assert (= __x0__ true)
[1874] OrdinarySet: Call[23949] app __x1__ = (O.GetOwnProperty O P)
[1875] OrdinaryObject.GetOwnProperty: Entry[23863]
[1876] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1877] OrdinaryGetOwnProperty: Entry[23788]
[1878] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1879] IsPropertyKey: Entry[21126]
[1880] IsPropertyKey: If[21127] (= (typeof argument) String)
[1881] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1882] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1883] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1884] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1885] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1886] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1887] IsDataDescriptor: Entry[21031]
[1888] IsDataDescriptor: If[21032] (= Desc undefined)
[1889] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1890] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1891] OrdinaryGetOwnProperty: If[23803] __x1__
[1892] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1893] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1894] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1895] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1896] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #49 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1897] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #49 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1898] OrdinarySet: Normal[23950] let ownDesc = [? __x1__]
[1899] OrdinarySet: Call[23945] app __x2__ = (OrdinarySetWithOwnDescriptor O P V Receiver ownDesc)
[1900] OrdinarySetWithOwnDescriptor: Entry[23974]
[1901] OrdinarySetWithOwnDescriptor: Call[23975] app __x0__ = (IsPropertyKey P)
[1902] IsPropertyKey: Entry[21126]
[1903] IsPropertyKey: If[21127] (= (typeof argument) String)
[1904] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1905] OrdinarySetWithOwnDescriptor: Normal[23983] assert (= __x0__ true)
[1906] OrdinarySetWithOwnDescriptor: If[23987] (= ownDesc undefined)
[1907] OrdinarySetWithOwnDescriptor: Call[23978] app __x3__ = (IsDataDescriptor ownDesc)
[1908] IsDataDescriptor: Entry[21031]
[1909] IsDataDescriptor: If[21032] (= Desc undefined)
[1910] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1911] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1912] OrdinarySetWithOwnDescriptor: If[23979] (= __x3__ true)
[1913] OrdinarySetWithOwnDescriptor: If[23988] (= ownDesc.Writable false)
[1914] OrdinarySetWithOwnDescriptor: If[23980] (! (= (typeof Receiver) Object))
[1915] OrdinarySetWithOwnDescriptor: Call[23982] app __x4__ = (Receiver.GetOwnProperty Receiver P)
[1916] OrdinaryObject.GetOwnProperty: Entry[23863]
[1917] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1918] OrdinaryGetOwnProperty: Entry[23788]
[1919] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1920] IsPropertyKey: Entry[21126]
[1921] IsPropertyKey: If[21127] (= (typeof argument) String)
[1922] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1923] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1924] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1925] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1926] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1927] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1928] IsDataDescriptor: Entry[21031]
[1929] IsDataDescriptor: If[21032] (= Desc undefined)
[1930] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1931] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1932] OrdinaryGetOwnProperty: If[23803] __x1__
[1933] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1934] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1935] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1936] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1937] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #50 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1938] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #50 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1939] OrdinarySetWithOwnDescriptor: Normal[24005] let existingDescriptor = [? __x4__]
[1940] OrdinarySetWithOwnDescriptor: If[23990] (! (= existingDescriptor undefined))
[1941] OrdinarySetWithOwnDescriptor: Call[23991] app __x5__ = (IsAccessorDescriptor existingDescriptor)
[1942] IsAccessorDescriptor: Entry[20967]
[1943] IsAccessorDescriptor: If[20968] (= Desc undefined)
[1944] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[1945] IsAccessorDescriptor: Normal[20973] return false
<RETURN> false
[1946] OrdinarySetWithOwnDescriptor: If[23998] (= __x5__ true)
[1947] OrdinarySetWithOwnDescriptor: If[24000] (= existingDescriptor.Writable false)
[1948] OrdinarySetWithOwnDescriptor: Normal[23995] let valueDesc = (new PropertyDescriptor("Value" -> V))
[1949] OrdinarySetWithOwnDescriptor: Call[23996] app __x6__ = (Receiver.DefineOwnProperty Receiver P valueDesc)
[1950] OrdinaryObject.DefineOwnProperty: Entry[23851]
[1951] OrdinaryObject.DefineOwnProperty: Call[23852] app __x0__ = (OrdinaryDefineOwnProperty O P Desc)
[1952] OrdinaryDefineOwnProperty: Entry[23715]
[1953] OrdinaryDefineOwnProperty: Call[23716] app __x0__ = (O.GetOwnProperty O P)
[1954] OrdinaryObject.GetOwnProperty: Entry[23863]
[1955] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[1956] OrdinaryGetOwnProperty: Entry[23788]
[1957] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[1958] IsPropertyKey: Entry[21126]
[1959] IsPropertyKey: If[21127] (= (typeof argument) String)
[1960] IsPropertyKey: Normal[21130] return true
<RETURN> true
[1961] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[1962] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[1963] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[1964] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[1965] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[1966] IsDataDescriptor: Entry[21031]
[1967] IsDataDescriptor: If[21032] (= Desc undefined)
[1968] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[1969] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[1970] OrdinaryGetOwnProperty: If[23803] __x1__
[1971] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[1972] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[1973] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[1974] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[1975] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #52 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1976] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #52 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> undefined
  "Configurable" -> false
}
[1977] OrdinaryDefineOwnProperty: Normal[23719] let current = [? __x0__]
[1978] OrdinaryDefineOwnProperty: Call[23721] app __x1__ = (IsExtensible O)
[1979] IsExtensible: Entry[21043]
[1980] IsExtensible: Normal[21044] assert (= (typeof O) Object)
[1981] IsExtensible: Call[21045] app __x0__ = (O.IsExtensible O)
[1982] OrdinaryObject.IsExtensible: Entry[23875]
[1983] OrdinaryObject.IsExtensible: Call[23876] app __x0__ = (OrdinaryIsExtensible O)
[1984] OrdinaryIsExtensible: Entry[23848]
[1985] OrdinaryIsExtensible: Normal[23849] return O.Extensible
<RETURN> true
[1986] OrdinaryObject.IsExtensible: Normal[23877] return [! __x0__]
<RETURN> true
[1987] IsExtensible: Normal[21046] return [? __x0__]
<RETURN> true
[1988] OrdinaryDefineOwnProperty: Normal[23722] let extensible = [? __x1__]
[1989] OrdinaryDefineOwnProperty: Call[23717] app __x2__ = (ValidateAndApplyPropertyDescriptor O P extensible Desc current)
[1990] ValidateAndApplyPropertyDescriptor: Entry[28891]
[1991] ValidateAndApplyPropertyDescriptor: If[28892] (= current undefined)
[1992] ValidateAndApplyPropertyDescriptor: If[28938] (&& (= absent Desc.Value) (&& (= absent Desc.Writable) (&& (= absent Desc.Get) (&& (= absent Desc.Set) (&& (= absent Desc.Enumerable) (= absent Desc.Configurable))))))
[1993] ValidateAndApplyPropertyDescriptor: If[28919] (= current.Configurable false)
[1994] ValidateAndApplyPropertyDescriptor: If[28989] (= Desc.Configurable true)
[1995] ValidateAndApplyPropertyDescriptor: Normal[28978] let __x4__ = true
[1996] ValidateAndApplyPropertyDescriptor: Normal[28992] __x4__ = (! (= Desc.Enumerable absent))
[1997] ValidateAndApplyPropertyDescriptor: If[28907] __x4__
[1998] ValidateAndApplyPropertyDescriptor: If[28909] __x4__
[1999] ValidateAndApplyPropertyDescriptor: Call[28898] app __x6__ = (IsGenericDescriptor Desc)
[2000] IsGenericDescriptor: Entry[21048]
[2001] IsGenericDescriptor: If[21049] (= Desc undefined)
[2002] IsGenericDescriptor: Call[21054] app __x0__ = (IsAccessorDescriptor Desc)
[2003] IsAccessorDescriptor: Entry[20967]
[2004] IsAccessorDescriptor: If[20968] (= Desc undefined)
[2005] IsAccessorDescriptor: If[20972] (&& (= Desc.Get absent) (= Desc.Set absent))
[2006] IsAccessorDescriptor: Normal[20973] return false
<RETURN> false
[2007] IsGenericDescriptor: Call[21056] app __x1__ = (IsDataDescriptor Desc)
[2008] IsDataDescriptor: Entry[21031]
[2009] IsDataDescriptor: If[21032] (= Desc undefined)
[2010] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2011] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2012] IsGenericDescriptor: If[21050] (&& (= __x0__ false) (= __x1__ false))
[2013] IsGenericDescriptor: Normal[21052] return false
<RETURN> false
[2014] ValidateAndApplyPropertyDescriptor: If[28923] (= [! __x6__] true)
[2015] ValidateAndApplyPropertyDescriptor: Call[28973] app __x7__ = (IsDataDescriptor current)
[2016] IsDataDescriptor: Entry[21031]
[2017] IsDataDescriptor: If[21032] (= Desc undefined)
[2018] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2019] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2020] ValidateAndApplyPropertyDescriptor: Call[28942] app __x8__ = (IsDataDescriptor Desc)
[2021] IsDataDescriptor: Entry[21031]
[2022] IsDataDescriptor: If[21032] (= Desc undefined)
[2023] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2024] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2025] ValidateAndApplyPropertyDescriptor: Call[28934] app __x9__ = (SameValue [! __x7__] [! __x8__])
[2026] SameValue: Entry[25946]
[2027] SameValue: If[25947] (! (= (typeof x) (typeof y)))
[2028] SameValue: If[25951] (|| (= (typeof x) Number) (= (typeof x) BigInt))
[2029] SameValue: Call[25949] app __x1__ = (SameValueNonNumeric x y)
[2030] SameValueNonNumeric: Entry[25955]
[2031] SameValueNonNumeric: Normal[25956] assert (! (|| (= (typeof x) Number) (= (typeof x) BigInt)))
[2032] SameValueNonNumeric: Normal[25966] assert (= (typeof x) (typeof y))
[2033] SameValueNonNumeric: If[25970] (= (typeof x) Undefined)
[2034] SameValueNonNumeric: If[25957] (= (typeof x) Null)
[2035] SameValueNonNumeric: If[25959] (= (typeof x) String)
[2036] SameValueNonNumeric: If[25967] (= (typeof x) Boolean)
[2037] SameValueNonNumeric: If[25960] (|| (&& (= x true) (= y true)) (&& (= x false) (= y false)))
[2038] SameValueNonNumeric: Normal[25961] return true
<RETURN> true
[2039] SameValue: Normal[25952] return [! __x1__]
<RETURN> true
[2040] ValidateAndApplyPropertyDescriptor: If[28935] (= [! __x9__] false)
[2041] ValidateAndApplyPropertyDescriptor: Call[28962] app __x11__ = (IsDataDescriptor current)
[2042] IsDataDescriptor: Entry[21031]
[2043] IsDataDescriptor: If[21032] (= Desc undefined)
[2044] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2045] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2046] ValidateAndApplyPropertyDescriptor: Call[28939] app __x12__ = (IsDataDescriptor Desc)
[2047] IsDataDescriptor: Entry[21031]
[2048] IsDataDescriptor: If[21032] (= Desc undefined)
[2049] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2050] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2051] ValidateAndApplyPropertyDescriptor: If[28940] (&& (= __x11__ true) (= __x12__ true))
[2052] ValidateAndApplyPropertyDescriptor: If[28981] (&& (= current.Configurable false) (= current.Writable false))
[2053] ValidateAndApplyPropertyDescriptor: If[28888] (! (= O undefined))
[2054] ValidateAndApplyPropertyDescriptor: Normal[28929] let __keys__ = (map-keys Desc)
[2055] ValidateAndApplyPropertyDescriptor: Normal[28987] let __i__ = 0i
[2056] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[2057] ValidateAndApplyPropertyDescriptor: Normal[28913] let __key__ = __keys__[__i__]
[2058] ValidateAndApplyPropertyDescriptor: Normal[28914] O.SubMap[P][__key__] = Desc[__key__]
[2059] ValidateAndApplyPropertyDescriptor: Normal[28885] __i__ = (+ __i__ 1i)
[2060] ValidateAndApplyPropertyDescriptor: LoopCont[28886]
[2061] ValidateAndApplyPropertyDescriptor: Loop[28958] (< __i__ __keys__.length)
[2062] ValidateAndApplyPropertyDescriptor: Normal[28930] return true
<RETURN> true
[2063] OrdinaryDefineOwnProperty: Normal[23718] return __x2__
<RETURN> N(true)
[2064] OrdinaryObject.DefineOwnProperty: Normal[23853] return [? __x0__]
<RETURN> true
[2065] OrdinarySetWithOwnDescriptor: Normal[23997] return [? __x6__]
<RETURN> true
[2066] OrdinarySet: Normal[23946] return __x2__
<RETURN> N(true)
[2067] OrdinaryObject.Set: Normal[23889] return [? __x0__]
<RETURN> true
[2068] Set: Normal[26223] let success = [? __x1__]
[2069] Set: If[26225] (&& (= success false) (= Throw true))
[2070] Set: Normal[26226] return success
<RETURN> true
[2071] ObjectEnvironmentRecord.SetMutableBinding: Normal[23506] return [? __x1__]
<RETURN> true
[2072] GlobalEnvironmentRecord.SetMutableBinding: Normal[19883] return [? __x2__]
<RETURN> true
[2073] PutValue: Normal[25285] return [? __x7__]
<RETURN> true
[2074] VariableDeclaration[0,1].Evaluation: Normal[29099] return [? __x6__]
<RETURN> true
[2075] VariableStatement[0,0].Evaluation: Normal[29128] let next = __x0__
[2076] VariableStatement[0,0].Evaluation: Normal[29129] [? next]
[2077] VariableStatement[0,0].Evaluation: Normal[29125] return ~empty~
<RETURN> ~empty~
[2078] StatementList[1,0].Evaluation: Normal[26878] let sl = __x0__
[2079] StatementList[1,0].Evaluation: Normal[26880] [? sl]
[2080] StatementList[1,0].Evaluation: Call[26882] access __x1__ = (StatementListItem "Evaluation")
[2081] ExpressionStatement[0,0].Evaluation: Entry[8759]
[2082] ExpressionStatement[0,0].Evaluation: Normal[8760] let ExpressionStatement = this
[2083] ExpressionStatement[0,0].Evaluation: Call[8763] access __x0__ = (Expression "Evaluation")
[2084] CallExpression[0,0].Evaluation: Entry[4075]
[2085] CallExpression[0,0].Evaluation: Normal[4076] let CallExpression = this
[2086] CallExpression[0,0].Evaluation: Call[4084] access __x0__ = (CoverCallExpressionAndAsyncArrowHead "CoveredCallExpression")
[2087] CoverCallExpressionAndAsyncArrowHead[0,0].CoveredCallExpression: Entry[6647]
[2088] CoverCallExpressionAndAsyncArrowHead[0,0].CoveredCallExpression: Normal[6648] let CoverCallExpressionAndAsyncArrowHead = this
[2089] CoverCallExpressionAndAsyncArrowHead[0,0].CoveredCallExpression: Normal[6649] return (parse-syntax CoverCallExpressionAndAsyncArrowHead "CallMemberExpression")
<RETURN> ☊[CallMemberExpression](print ( x ))
[2090] CallExpression[0,0].Evaluation: Normal[4088] let expr = __x0__
[2091] CallExpression[0,0].Evaluation: Call[4092] access __x1__ = (expr "MemberExpression")
[2092] CallExpression[0,0].Evaluation: Normal[4077] let memberExpr = __x1__
[2093] CallExpression[0,0].Evaluation: Call[4078] access __x2__ = (expr "Arguments")
[2094] CallExpression[0,0].Evaluation: Normal[4085] let arguments = __x2__
[2095] CallExpression[0,0].Evaluation: Call[4090] access __x3__ = (memberExpr "Evaluation")
[2096] IdentifierReference[0,0].Evaluation: Entry[20026]
[2097] IdentifierReference[0,0].Evaluation: Normal[20027] let IdentifierReference = this
[2098] IdentifierReference[0,0].Evaluation: Call[20028] access __x0__ = (Identifier "StringValue")
[2099] Identifier[0,0].StringValue: Entry[20090]
[2100] Identifier[0,0].StringValue: Normal[20091] let Identifier = this
[2101] Identifier[0,0].StringValue: Call[20092] access __x0__ = (IdentifierName "StringValue")
[2102] Identifier[0,0].StringValue: Normal[20093] return __x0__
<RETURN> "print"
[2103] IdentifierReference[0,0].Evaluation: Call[20029] app __x1__ = (ResolveBinding __x0__)
[2104] ResolveBinding: Entry[25799]
[2105] ResolveBinding: If[25800] (|| (= env absent) (= env undefined))
[2106] ResolveBinding: Normal[25803] env = CONTEXT.LexicalEnvironment
[2107] ResolveBinding: Normal[25804] assert (is-instance-of env EnvironmentRecord)
[2108] ResolveBinding: If[25807] true
[2109] ResolveBinding: Normal[25801] let strict = true
[2110] ResolveBinding: Call[25802] app __x0__ = (GetIdentifierReference env name strict)
[2111] GetIdentifierReference: Entry[19317]
[2112] GetIdentifierReference: If[19318] (= env null)
[2113] GetIdentifierReference: Call[19323] app __x0__ = (env.HasBinding env name)
[2114] GlobalEnvironmentRecord.HasBinding: Entry[19829]
[2115] GlobalEnvironmentRecord.HasBinding: Normal[19830] let DclRec = envRec.DeclarativeRecord
[2116] GlobalEnvironmentRecord.HasBinding: Call[19833] app __x0__ = (DclRec.HasBinding DclRec N)
[2117] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[2118] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[2119] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[2120] GlobalEnvironmentRecord.HasBinding: If[19835] (= __x0__ true)
[2121] GlobalEnvironmentRecord.HasBinding: Normal[19831] let ObjRec = envRec.ObjectRecord
[2122] GlobalEnvironmentRecord.HasBinding: Call[19832] app __x1__ = (ObjRec.HasBinding ObjRec N)
[2123] ObjectEnvironmentRecord.HasBinding: Entry[23473]
[2124] ObjectEnvironmentRecord.HasBinding: Normal[23474] let bindings = envRec.BindingObject
[2125] ObjectEnvironmentRecord.HasBinding: Call[23482] app __x0__ = (HasProperty bindings N)
[2126] HasProperty: Entry[19899]
[2127] HasProperty: Normal[19900] assert (= (typeof O) Object)
[2128] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[2129] IsPropertyKey: Entry[21126]
[2130] IsPropertyKey: If[21127] (= (typeof argument) String)
[2131] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2132] HasProperty: Normal[19904] assert (= __x0__ true)
[2133] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[2134] OrdinaryObject.HasProperty: Entry[23871]
[2135] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[2136] OrdinaryHasProperty: Entry[23834]
[2137] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[2138] IsPropertyKey: Entry[21126]
[2139] IsPropertyKey: If[21127] (= (typeof argument) String)
[2140] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2141] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[2142] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[2143] OrdinaryObject.GetOwnProperty: Entry[23863]
[2144] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[2145] OrdinaryGetOwnProperty: Entry[23788]
[2146] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[2147] IsPropertyKey: Entry[21126]
[2148] IsPropertyKey: If[21127] (= (typeof argument) String)
[2149] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2150] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[2151] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[2152] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[2153] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[2154] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[2155] IsDataDescriptor: Entry[21031]
[2156] IsDataDescriptor: If[21032] (= Desc undefined)
[2157] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2158] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2159] OrdinaryGetOwnProperty: If[23803] __x1__
[2160] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[2161] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[2162] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[2163] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[2164] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #54 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> false
  "Writable" -> true
  "Value" -> #GLOBAL.print
  "Configurable" -> true
}
[2165] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #54 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> false
  "Writable" -> true
  "Value" -> #GLOBAL.print
  "Configurable" -> true
}
[2166] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[2167] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[2168] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[2169] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[2170] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[2171] ObjectEnvironmentRecord.HasBinding: Normal[23487] let foundBinding = [? __x0__]
[2172] ObjectEnvironmentRecord.HasBinding: If[23489] (= foundBinding false)
[2173] ObjectEnvironmentRecord.HasBinding: If[23476] (= envRec.withEnvironment false)
[2174] ObjectEnvironmentRecord.HasBinding: Normal[23483] return true
<RETURN> true
[2175] GlobalEnvironmentRecord.HasBinding: Normal[19834] return [? __x1__]
<RETURN> true
[2176] GetIdentifierReference: Normal[19327] let exists = [? __x0__]
[2177] GetIdentifierReference: If[19319] (= exists true)
[2178] GetIdentifierReference: Normal[19320] return (new ReferenceRecord("Base" -> env, "ReferencedName" -> name, "Strict" -> strict, "ThisValue" -> ~empty~))
<RETURN> #55 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("print")
}
[2179] ResolveBinding: Normal[25806] return [? __x0__]
<RETURN> #55 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("print")
}
[2180] IdentifierReference[0,0].Evaluation: Normal[20030] return [? __x1__]
<RETURN> #55 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("print")
}
[2181] CallExpression[0,0].Evaluation: Normal[4086] let ref = __x3__
[2182] CallExpression[0,0].Evaluation: Call[4079] app __x4__ = (GetValue ref)
[2183] GetValue: Entry[19545]
[2184] GetValue: Normal[19546] [? V]
[2185] GetValue: If[19554] (! (is-instance-of V ReferenceRecord))
[2186] GetValue: Call[19559] app __x0__ = (IsUnresolvableReference V)
[2187] IsUnresolvableReference: Entry[21178]
[2188] IsUnresolvableReference: Normal[21179] assert (is-instance-of V ReferenceRecord)
[2189] IsUnresolvableReference: If[21180] (= V.Base ~unresolvable~)
[2190] IsUnresolvableReference: Normal[21182] return false
<RETURN> false
[2191] GetValue: If[19547] (= __x0__ true)
[2192] GetValue: Call[19549] app __x1__ = (IsPropertyReference V)
[2193] IsPropertyReference: Entry[21133]
[2194] IsPropertyReference: Normal[21134] assert (is-instance-of V ReferenceRecord)
[2195] IsPropertyReference: If[21137] (= V.Base ~unresolvable~)
[2196] IsPropertyReference: If[21140] (|| (|| (|| (|| (|| (= (typeof V.Base) Boolean) (= (typeof V.Base) String)) (= (typeof V.Base) Symbol)) (= (typeof V.Base) BigInt)) (= (typeof V.Base) Number)) (= (typeof V.Base) Object))
[2197] IsPropertyReference: Normal[21138] return false
<RETURN> false
[2198] GetValue: If[19562] (= __x1__ true)
[2199] GetValue: Normal[19552] let base = V.Base
[2200] GetValue: Normal[19553] assert (is-instance-of base EnvironmentRecord)
[2201] GetValue: Call[19563] app __x5__ = (base.GetBindingValue base V.ReferencedName V.Strict)
[2202] GlobalEnvironmentRecord.GetBindingValue: Entry[19816]
[2203] GlobalEnvironmentRecord.GetBindingValue: Normal[19817] let DclRec = envRec.DeclarativeRecord
[2204] GlobalEnvironmentRecord.GetBindingValue: Call[19820] app __x0__ = (DclRec.HasBinding DclRec N)
[2205] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[2206] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[2207] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[2208] GlobalEnvironmentRecord.GetBindingValue: If[19822] (= __x0__ true)
[2209] GlobalEnvironmentRecord.GetBindingValue: Normal[19819] let ObjRec = envRec.ObjectRecord
[2210] GlobalEnvironmentRecord.GetBindingValue: Call[19821] app __x2__ = (ObjRec.GetBindingValue ObjRec N S)
[2211] ObjectEnvironmentRecord.GetBindingValue: Entry[23462]
[2212] ObjectEnvironmentRecord.GetBindingValue: Normal[23463] let bindings = envRec.BindingObject
[2213] ObjectEnvironmentRecord.GetBindingValue: Call[23467] app __x0__ = (HasProperty bindings N)
[2214] HasProperty: Entry[19899]
[2215] HasProperty: Normal[19900] assert (= (typeof O) Object)
[2216] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[2217] IsPropertyKey: Entry[21126]
[2218] IsPropertyKey: If[21127] (= (typeof argument) String)
[2219] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2220] HasProperty: Normal[19904] assert (= __x0__ true)
[2221] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[2222] OrdinaryObject.HasProperty: Entry[23871]
[2223] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[2224] OrdinaryHasProperty: Entry[23834]
[2225] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[2226] IsPropertyKey: Entry[21126]
[2227] IsPropertyKey: If[21127] (= (typeof argument) String)
[2228] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2229] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[2230] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[2231] OrdinaryObject.GetOwnProperty: Entry[23863]
[2232] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[2233] OrdinaryGetOwnProperty: Entry[23788]
[2234] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[2235] IsPropertyKey: Entry[21126]
[2236] IsPropertyKey: If[21127] (= (typeof argument) String)
[2237] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2238] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[2239] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[2240] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[2241] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[2242] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[2243] IsDataDescriptor: Entry[21031]
[2244] IsDataDescriptor: If[21032] (= Desc undefined)
[2245] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2246] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2247] OrdinaryGetOwnProperty: If[23803] __x1__
[2248] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[2249] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[2250] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[2251] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[2252] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #56 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> false
  "Writable" -> true
  "Value" -> #GLOBAL.print
  "Configurable" -> true
}
[2253] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #56 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> false
  "Writable" -> true
  "Value" -> #GLOBAL.print
  "Configurable" -> true
}
[2254] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[2255] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[2256] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[2257] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[2258] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[2259] ObjectEnvironmentRecord.GetBindingValue: Normal[23471] let value = [? __x0__]
[2260] ObjectEnvironmentRecord.GetBindingValue: If[23472] (= value false)
[2261] ObjectEnvironmentRecord.GetBindingValue: Call[23468] app __x1__ = (Get bindings N)
[2262] Get: Entry[19222]
[2263] Get: Normal[19223] assert (= (typeof O) Object)
[2264] Get: Call[19226] app __x0__ = (IsPropertyKey P)
[2265] IsPropertyKey: Entry[21126]
[2266] IsPropertyKey: If[21127] (= (typeof argument) String)
[2267] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2268] Get: Normal[19227] assert (= __x0__ true)
[2269] Get: Call[19228] app __x1__ = (O.Get O P O)
[2270] OrdinaryObject.Get: Entry[23859]
[2271] OrdinaryObject.Get: Call[23860] app __x0__ = (OrdinaryGet O P Receiver)
[2272] OrdinaryGet: Entry[23765]
[2273] OrdinaryGet: Call[23766] app __x0__ = (IsPropertyKey P)
[2274] IsPropertyKey: Entry[21126]
[2275] IsPropertyKey: If[21127] (= (typeof argument) String)
[2276] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2277] OrdinaryGet: Normal[23776] assert (= __x0__ true)
[2278] OrdinaryGet: Call[23781] app __x1__ = (O.GetOwnProperty O P)
[2279] OrdinaryObject.GetOwnProperty: Entry[23863]
[2280] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[2281] OrdinaryGetOwnProperty: Entry[23788]
[2282] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[2283] IsPropertyKey: Entry[21126]
[2284] IsPropertyKey: If[21127] (= (typeof argument) String)
[2285] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2286] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[2287] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[2288] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[2289] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[2290] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[2291] IsDataDescriptor: Entry[21031]
[2292] IsDataDescriptor: If[21032] (= Desc undefined)
[2293] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2294] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2295] OrdinaryGetOwnProperty: If[23803] __x1__
[2296] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[2297] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[2298] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[2299] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[2300] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #57 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> false
  "Writable" -> true
  "Value" -> #GLOBAL.print
  "Configurable" -> true
}
[2301] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #57 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> false
  "Writable" -> true
  "Value" -> #GLOBAL.print
  "Configurable" -> true
}
[2302] OrdinaryGet: Normal[23785] let desc = [? __x1__]
[2303] OrdinaryGet: If[23767] (= desc undefined)
[2304] OrdinaryGet: Call[23769] app __x4__ = (IsDataDescriptor desc)
[2305] IsDataDescriptor: Entry[21031]
[2306] IsDataDescriptor: If[21032] (= Desc undefined)
[2307] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2308] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2309] OrdinaryGet: If[23780] (= __x4__ true)
[2310] OrdinaryGet: Normal[23772] return desc.Value
<RETURN> #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Function.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "Call" -> λ(BuiltinFunctionObject.Call)
  "SubMap" -> #GLOBAL.print.SubMap
  "Code" -> λ(GLOBAL.HostPrint)
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[2311] OrdinaryObject.Get: Normal[23861] return [? __x0__]
<RETURN> #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Function.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "Call" -> λ(BuiltinFunctionObject.Call)
  "SubMap" -> #GLOBAL.print.SubMap
  "Code" -> λ(GLOBAL.HostPrint)
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[2312] Get: Normal[19224] return [? __x1__]
<RETURN> #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Function.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "Call" -> λ(BuiltinFunctionObject.Call)
  "SubMap" -> #GLOBAL.print.SubMap
  "Code" -> λ(GLOBAL.HostPrint)
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[2313] ObjectEnvironmentRecord.GetBindingValue: Normal[23469] return [? __x1__]
<RETURN> #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Function.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "Call" -> λ(BuiltinFunctionObject.Call)
  "SubMap" -> #GLOBAL.print.SubMap
  "Code" -> λ(GLOBAL.HostPrint)
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[2314] GlobalEnvironmentRecord.GetBindingValue: Normal[19823] return [? __x2__]
<RETURN> #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Function.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "Call" -> λ(BuiltinFunctionObject.Call)
  "SubMap" -> #GLOBAL.print.SubMap
  "Code" -> λ(GLOBAL.HostPrint)
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[2315] GetValue: Normal[19560] return [? __x5__]
<RETURN> #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
  "HasProperty" -> λ(OrdinaryObject.HasProperty)
  "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
  "Delete" -> λ(OrdinaryObject.Delete)
  "Prototype" -> #GLOBAL.Function.prototype
  "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
  "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
  "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
  "Call" -> λ(BuiltinFunctionObject.Call)
  "SubMap" -> #GLOBAL.print.SubMap
  "Code" -> λ(GLOBAL.HostPrint)
  "Get" -> λ(OrdinaryObject.Get)
  "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
  "Extensible" -> true
  "Set" -> λ(OrdinaryObject.Set)
  "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
  "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
}
[2316] CallExpression[0,0].Evaluation: Normal[4080] let func = [? __x4__]
[2317] CallExpression[0,0].Evaluation: Normal[4089] let __x5__ = true
[2318] CallExpression[0,0].Evaluation: Normal[4087] __x5__ = (is-instance-of ref ReferenceRecord)
[2319] CallExpression[0,0].Evaluation: If[4081] __x5__
[2320] CallExpression[0,0].Evaluation: Call[4082] app __x6__ = (IsPropertyReference ref)
[2321] IsPropertyReference: Entry[21133]
[2322] IsPropertyReference: Normal[21134] assert (is-instance-of V ReferenceRecord)
[2323] IsPropertyReference: If[21137] (= V.Base ~unresolvable~)
[2324] IsPropertyReference: If[21140] (|| (|| (|| (|| (|| (= (typeof V.Base) Boolean) (= (typeof V.Base) String)) (= (typeof V.Base) Symbol)) (= (typeof V.Base) BigInt)) (= (typeof V.Base) Number)) (= (typeof V.Base) Object))
[2325] IsPropertyReference: Normal[21138] return false
<RETURN> false
[2326] CallExpression[0,0].Evaluation: Normal[4093] __x5__ = (= __x6__ false)
[2327] CallExpression[0,0].Evaluation: If[4107] __x5__
[2328] CallExpression[0,0].Evaluation: Normal[4091] __x5__ = (= ref.ReferencedName "eval")
[2329] CallExpression[0,0].Evaluation: If[4083] __x5__
[2330] CallExpression[0,0].Evaluation: Normal[4105] let thisCall = this
[2331] CallExpression[0,0].Evaluation: Call[4106] app __x10__ = (IsInTailPosition thisCall)
[2332] IsInTailPosition: Entry[21057]
[2333] IsInTailPosition: If[21058] false
[2334] IsInTailPosition: Normal[21069] let __c__ = false
[2335] IsInTailPosition: Normal[21079] let __b__ = call
[2336] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2337] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2338] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2339] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2340] IsInTailPosition: If[21073] (! __c__)
[2341] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2342] IsInTailPosition: LoopCont[21063]
[2343] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2344] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2345] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2346] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2347] IsInTailPosition: If[21073] (! __c__)
[2348] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2349] IsInTailPosition: LoopCont[21063]
[2350] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2351] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2352] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2353] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2354] IsInTailPosition: If[21073] (! __c__)
[2355] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2356] IsInTailPosition: LoopCont[21063]
[2357] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2358] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2359] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2360] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2361] IsInTailPosition: If[21073] (! __c__)
[2362] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2363] IsInTailPosition: LoopCont[21063]
[2364] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2365] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2366] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2367] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2368] IsInTailPosition: If[21073] (! __c__)
[2369] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2370] IsInTailPosition: LoopCont[21063]
[2371] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2372] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2373] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2374] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2375] IsInTailPosition: If[21073] (! __c__)
[2376] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2377] IsInTailPosition: LoopCont[21063]
[2378] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2379] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2380] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2381] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2382] IsInTailPosition: If[21073] (! __c__)
[2383] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2384] IsInTailPosition: LoopCont[21063]
[2385] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2386] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2387] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2388] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2389] IsInTailPosition: If[21073] (! __c__)
[2390] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2391] IsInTailPosition: LoopCont[21063]
[2392] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2393] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2394] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2395] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2396] IsInTailPosition: If[21073] (! __c__)
[2397] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2398] IsInTailPosition: LoopCont[21063]
[2399] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2400] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2401] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2402] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2403] IsInTailPosition: If[21073] (! __c__)
[2404] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2405] IsInTailPosition: LoopCont[21063]
[2406] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2407] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2408] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2409] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2410] IsInTailPosition: If[21073] (! __c__)
[2411] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2412] IsInTailPosition: LoopCont[21063]
[2413] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2414] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2415] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2416] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2417] IsInTailPosition: If[21073] (! __c__)
[2418] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2419] IsInTailPosition: LoopCont[21063]
[2420] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2421] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2422] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2423] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2424] IsInTailPosition: If[21073] (! __c__)
[2425] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2426] IsInTailPosition: LoopCont[21063]
[2427] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2428] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2429] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2430] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2431] IsInTailPosition: If[21073] (! __c__)
[2432] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2433] IsInTailPosition: LoopCont[21063]
[2434] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2435] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2436] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2437] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2438] IsInTailPosition: If[21073] (! __c__)
[2439] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2440] IsInTailPosition: LoopCont[21063]
[2441] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2442] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2443] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2444] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2445] IsInTailPosition: If[21073] (! __c__)
[2446] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2447] IsInTailPosition: LoopCont[21063]
[2448] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2449] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2450] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2451] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2452] IsInTailPosition: If[21073] (! __c__)
[2453] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2454] IsInTailPosition: LoopCont[21063]
[2455] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2456] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2457] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2458] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2459] IsInTailPosition: If[21073] (! __c__)
[2460] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2461] IsInTailPosition: LoopCont[21063]
[2462] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2463] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2464] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2465] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2466] IsInTailPosition: If[21073] (! __c__)
[2467] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2468] IsInTailPosition: LoopCont[21063]
[2469] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2470] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2471] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2472] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2473] IsInTailPosition: If[21073] (! __c__)
[2474] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2475] IsInTailPosition: LoopCont[21063]
[2476] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2477] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2478] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2479] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2480] IsInTailPosition: If[21073] (! __c__)
[2481] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2482] IsInTailPosition: LoopCont[21063]
[2483] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2484] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2485] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2486] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2487] IsInTailPosition: If[21073] (! __c__)
[2488] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2489] IsInTailPosition: LoopCont[21063]
[2490] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2491] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2492] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2493] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2494] IsInTailPosition: If[21073] (! __c__)
[2495] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2496] IsInTailPosition: LoopCont[21063]
[2497] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2498] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2499] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2500] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2501] IsInTailPosition: If[21073] (! __c__)
[2502] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2503] IsInTailPosition: LoopCont[21063]
[2504] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2505] IsInTailPosition: Normal[21060] __c__ = (|| __c__ (is-instance-of __b__ FunctionBody))
[2506] IsInTailPosition: Normal[21070] __c__ = (|| __c__ (is-instance-of __b__ ConciseBody))
[2507] IsInTailPosition: Normal[21078] __c__ = (|| __c__ (is-instance-of __b__ AsyncConciseBody))
[2508] IsInTailPosition: If[21073] (! __c__)
[2509] IsInTailPosition: Call[21062] access __b__ = (__b__ "parent")
[2510] IsInTailPosition: LoopCont[21063]
[2511] IsInTailPosition: Loop[21059] (&& (! __c__) (! (= __b__ absent)))
[2512] IsInTailPosition: If[21061] (! __c__)
[2513] IsInTailPosition: Normal[21074] return false
<RETURN> false
[2514] CallExpression[0,0].Evaluation: Normal[4109] let tailCall = __x10__
[2515] CallExpression[0,0].Evaluation: Call[4112] app __x11__ = (EvaluateCall func ref arguments tailCall)
[2516] EvaluateCall: Entry[8210]
[2517] EvaluateCall: If[8211] (is-instance-of ref ReferenceRecord)
[2518] EvaluateCall: Call[8219] app __x0__ = (IsPropertyReference ref)
[2519] IsPropertyReference: Entry[21133]
[2520] IsPropertyReference: Normal[21134] assert (is-instance-of V ReferenceRecord)
[2521] IsPropertyReference: If[21137] (= V.Base ~unresolvable~)
[2522] IsPropertyReference: If[21140] (|| (|| (|| (|| (|| (= (typeof V.Base) Boolean) (= (typeof V.Base) String)) (= (typeof V.Base) Symbol)) (= (typeof V.Base) BigInt)) (= (typeof V.Base) Number)) (= (typeof V.Base) Object))
[2523] IsPropertyReference: Normal[21138] return false
<RETURN> false
[2524] EvaluateCall: If[8225] (= __x0__ true)
[2525] EvaluateCall: Normal[8220] let refEnv = ref.Base
[2526] EvaluateCall: Normal[8221] assert (is-instance-of refEnv EnvironmentRecord)
[2527] EvaluateCall: Call[8230] app __x2__ = (refEnv.WithBaseObject refEnv)
[2528] GlobalEnvironmentRecord.WithBaseObject: Entry[19886]
[2529] GlobalEnvironmentRecord.WithBaseObject: Normal[19887] return undefined
<RETURN> undefined
[2530] EvaluateCall: Normal[8223] let thisValue = __x2__
[2531] EvaluateCall: Call[8213] access __x3__ = (arguments "ArgumentListEvaluation")
[2532] ArgumentList[0,0].ArgumentListEvaluation: Entry[344]
[2533] ArgumentList[0,0].ArgumentListEvaluation: Normal[345] let ArgumentList = this
[2534] ArgumentList[0,0].ArgumentListEvaluation: Call[348] access __x0__ = (AssignmentExpression "Evaluation")
[2535] IdentifierReference[0,0].Evaluation: Entry[20026]
[2536] IdentifierReference[0,0].Evaluation: Normal[20027] let IdentifierReference = this
[2537] IdentifierReference[0,0].Evaluation: Call[20028] access __x0__ = (Identifier "StringValue")
[2538] Identifier[0,0].StringValue: Entry[20090]
[2539] Identifier[0,0].StringValue: Normal[20091] let Identifier = this
[2540] Identifier[0,0].StringValue: Call[20092] access __x0__ = (IdentifierName "StringValue")
[2541] Identifier[0,0].StringValue: Normal[20093] return __x0__
<RETURN> "x"
[2542] IdentifierReference[0,0].Evaluation: Call[20029] app __x1__ = (ResolveBinding __x0__)
[2543] ResolveBinding: Entry[25799]
[2544] ResolveBinding: If[25800] (|| (= env absent) (= env undefined))
[2545] ResolveBinding: Normal[25803] env = CONTEXT.LexicalEnvironment
[2546] ResolveBinding: Normal[25804] assert (is-instance-of env EnvironmentRecord)
[2547] ResolveBinding: If[25807] true
[2548] ResolveBinding: Normal[25801] let strict = true
[2549] ResolveBinding: Call[25802] app __x0__ = (GetIdentifierReference env name strict)
[2550] GetIdentifierReference: Entry[19317]
[2551] GetIdentifierReference: If[19318] (= env null)
[2552] GetIdentifierReference: Call[19323] app __x0__ = (env.HasBinding env name)
[2553] GlobalEnvironmentRecord.HasBinding: Entry[19829]
[2554] GlobalEnvironmentRecord.HasBinding: Normal[19830] let DclRec = envRec.DeclarativeRecord
[2555] GlobalEnvironmentRecord.HasBinding: Call[19833] app __x0__ = (DclRec.HasBinding DclRec N)
[2556] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[2557] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[2558] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[2559] GlobalEnvironmentRecord.HasBinding: If[19835] (= __x0__ true)
[2560] GlobalEnvironmentRecord.HasBinding: Normal[19831] let ObjRec = envRec.ObjectRecord
[2561] GlobalEnvironmentRecord.HasBinding: Call[19832] app __x1__ = (ObjRec.HasBinding ObjRec N)
[2562] ObjectEnvironmentRecord.HasBinding: Entry[23473]
[2563] ObjectEnvironmentRecord.HasBinding: Normal[23474] let bindings = envRec.BindingObject
[2564] ObjectEnvironmentRecord.HasBinding: Call[23482] app __x0__ = (HasProperty bindings N)
[2565] HasProperty: Entry[19899]
[2566] HasProperty: Normal[19900] assert (= (typeof O) Object)
[2567] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[2568] IsPropertyKey: Entry[21126]
[2569] IsPropertyKey: If[21127] (= (typeof argument) String)
[2570] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2571] HasProperty: Normal[19904] assert (= __x0__ true)
[2572] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[2573] OrdinaryObject.HasProperty: Entry[23871]
[2574] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[2575] OrdinaryHasProperty: Entry[23834]
[2576] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[2577] IsPropertyKey: Entry[21126]
[2578] IsPropertyKey: If[21127] (= (typeof argument) String)
[2579] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2580] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[2581] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[2582] OrdinaryObject.GetOwnProperty: Entry[23863]
[2583] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[2584] OrdinaryGetOwnProperty: Entry[23788]
[2585] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[2586] IsPropertyKey: Entry[21126]
[2587] IsPropertyKey: If[21127] (= (typeof argument) String)
[2588] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2589] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[2590] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[2591] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[2592] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[2593] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[2594] IsDataDescriptor: Entry[21031]
[2595] IsDataDescriptor: If[21032] (= Desc undefined)
[2596] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2597] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2598] OrdinaryGetOwnProperty: If[23803] __x1__
[2599] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[2600] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[2601] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[2602] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[2603] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #58 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> 3.0
  "Configurable" -> false
}
[2604] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #58 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> 3.0
  "Configurable" -> false
}
[2605] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[2606] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[2607] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[2608] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[2609] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[2610] ObjectEnvironmentRecord.HasBinding: Normal[23487] let foundBinding = [? __x0__]
[2611] ObjectEnvironmentRecord.HasBinding: If[23489] (= foundBinding false)
[2612] ObjectEnvironmentRecord.HasBinding: If[23476] (= envRec.withEnvironment false)
[2613] ObjectEnvironmentRecord.HasBinding: Normal[23483] return true
<RETURN> true
[2614] GlobalEnvironmentRecord.HasBinding: Normal[19834] return [? __x1__]
<RETURN> true
[2615] GetIdentifierReference: Normal[19327] let exists = [? __x0__]
[2616] GetIdentifierReference: If[19319] (= exists true)
[2617] GetIdentifierReference: Normal[19320] return (new ReferenceRecord("Base" -> env, "ReferencedName" -> name, "Strict" -> strict, "ThisValue" -> ~empty~))
<RETURN> #59 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("x")
}
[2618] ResolveBinding: Normal[25806] return [? __x0__]
<RETURN> #59 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("x")
}
[2619] IdentifierReference[0,0].Evaluation: Normal[20030] return [? __x1__]
<RETURN> #59 -> (TYPE = ReferenceRecord) {
  "ThisValue" -> ~empty~
  "Base" -> N(#17)
  "Strict" -> true
  "ReferencedName" -> N("x")
}
[2620] ArgumentList[0,0].ArgumentListEvaluation: Normal[350] let ref = __x0__
[2621] ArgumentList[0,0].ArgumentListEvaluation: Call[351] app __x1__ = (GetValue ref)
[2622] GetValue: Entry[19545]
[2623] GetValue: Normal[19546] [? V]
[2624] GetValue: If[19554] (! (is-instance-of V ReferenceRecord))
[2625] GetValue: Call[19559] app __x0__ = (IsUnresolvableReference V)
[2626] IsUnresolvableReference: Entry[21178]
[2627] IsUnresolvableReference: Normal[21179] assert (is-instance-of V ReferenceRecord)
[2628] IsUnresolvableReference: If[21180] (= V.Base ~unresolvable~)
[2629] IsUnresolvableReference: Normal[21182] return false
<RETURN> false
[2630] GetValue: If[19547] (= __x0__ true)
[2631] GetValue: Call[19549] app __x1__ = (IsPropertyReference V)
[2632] IsPropertyReference: Entry[21133]
[2633] IsPropertyReference: Normal[21134] assert (is-instance-of V ReferenceRecord)
[2634] IsPropertyReference: If[21137] (= V.Base ~unresolvable~)
[2635] IsPropertyReference: If[21140] (|| (|| (|| (|| (|| (= (typeof V.Base) Boolean) (= (typeof V.Base) String)) (= (typeof V.Base) Symbol)) (= (typeof V.Base) BigInt)) (= (typeof V.Base) Number)) (= (typeof V.Base) Object))
[2636] IsPropertyReference: Normal[21138] return false
<RETURN> false
[2637] GetValue: If[19562] (= __x1__ true)
[2638] GetValue: Normal[19552] let base = V.Base
[2639] GetValue: Normal[19553] assert (is-instance-of base EnvironmentRecord)
[2640] GetValue: Call[19563] app __x5__ = (base.GetBindingValue base V.ReferencedName V.Strict)
[2641] GlobalEnvironmentRecord.GetBindingValue: Entry[19816]
[2642] GlobalEnvironmentRecord.GetBindingValue: Normal[19817] let DclRec = envRec.DeclarativeRecord
[2643] GlobalEnvironmentRecord.GetBindingValue: Call[19820] app __x0__ = (DclRec.HasBinding DclRec N)
[2644] DeclarativeEnvironmentRecord.HasBinding: Entry[7374]
[2645] DeclarativeEnvironmentRecord.HasBinding: If[7375] (= envRec.SubMap[N] absent)
[2646] DeclarativeEnvironmentRecord.HasBinding: Normal[7376] return false
<RETURN> false
[2647] GlobalEnvironmentRecord.GetBindingValue: If[19822] (= __x0__ true)
[2648] GlobalEnvironmentRecord.GetBindingValue: Normal[19819] let ObjRec = envRec.ObjectRecord
[2649] GlobalEnvironmentRecord.GetBindingValue: Call[19821] app __x2__ = (ObjRec.GetBindingValue ObjRec N S)
[2650] ObjectEnvironmentRecord.GetBindingValue: Entry[23462]
[2651] ObjectEnvironmentRecord.GetBindingValue: Normal[23463] let bindings = envRec.BindingObject
[2652] ObjectEnvironmentRecord.GetBindingValue: Call[23467] app __x0__ = (HasProperty bindings N)
[2653] HasProperty: Entry[19899]
[2654] HasProperty: Normal[19900] assert (= (typeof O) Object)
[2655] HasProperty: Call[19903] app __x0__ = (IsPropertyKey P)
[2656] IsPropertyKey: Entry[21126]
[2657] IsPropertyKey: If[21127] (= (typeof argument) String)
[2658] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2659] HasProperty: Normal[19904] assert (= __x0__ true)
[2660] HasProperty: Call[19905] app __x1__ = (O.HasProperty O P)
[2661] OrdinaryObject.HasProperty: Entry[23871]
[2662] OrdinaryObject.HasProperty: Call[23872] app __x0__ = (OrdinaryHasProperty O P)
[2663] OrdinaryHasProperty: Entry[23834]
[2664] OrdinaryHasProperty: Call[23835] app __x0__ = (IsPropertyKey P)
[2665] IsPropertyKey: Entry[21126]
[2666] IsPropertyKey: If[21127] (= (typeof argument) String)
[2667] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2668] OrdinaryHasProperty: Normal[23841] assert (= __x0__ true)
[2669] OrdinaryHasProperty: Call[23844] app __x1__ = (O.GetOwnProperty O P)
[2670] OrdinaryObject.GetOwnProperty: Entry[23863]
[2671] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[2672] OrdinaryGetOwnProperty: Entry[23788]
[2673] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[2674] IsPropertyKey: Entry[21126]
[2675] IsPropertyKey: If[21127] (= (typeof argument) String)
[2676] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2677] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[2678] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[2679] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[2680] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[2681] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[2682] IsDataDescriptor: Entry[21031]
[2683] IsDataDescriptor: If[21032] (= Desc undefined)
[2684] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2685] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2686] OrdinaryGetOwnProperty: If[23803] __x1__
[2687] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[2688] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[2689] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[2690] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[2691] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #60 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> 3.0
  "Configurable" -> false
}
[2692] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #60 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> 3.0
  "Configurable" -> false
}
[2693] OrdinaryHasProperty: Normal[23847] let hasOwn = [? __x1__]
[2694] OrdinaryHasProperty: If[23836] (! (= hasOwn undefined))
[2695] OrdinaryHasProperty: Normal[23837] return true
<RETURN> true
[2696] OrdinaryObject.HasProperty: Normal[23873] return [? __x0__]
<RETURN> true
[2697] HasProperty: Normal[19901] return [? __x1__]
<RETURN> true
[2698] ObjectEnvironmentRecord.GetBindingValue: Normal[23471] let value = [? __x0__]
[2699] ObjectEnvironmentRecord.GetBindingValue: If[23472] (= value false)
[2700] ObjectEnvironmentRecord.GetBindingValue: Call[23468] app __x1__ = (Get bindings N)
[2701] Get: Entry[19222]
[2702] Get: Normal[19223] assert (= (typeof O) Object)
[2703] Get: Call[19226] app __x0__ = (IsPropertyKey P)
[2704] IsPropertyKey: Entry[21126]
[2705] IsPropertyKey: If[21127] (= (typeof argument) String)
[2706] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2707] Get: Normal[19227] assert (= __x0__ true)
[2708] Get: Call[19228] app __x1__ = (O.Get O P O)
[2709] OrdinaryObject.Get: Entry[23859]
[2710] OrdinaryObject.Get: Call[23860] app __x0__ = (OrdinaryGet O P Receiver)
[2711] OrdinaryGet: Entry[23765]
[2712] OrdinaryGet: Call[23766] app __x0__ = (IsPropertyKey P)
[2713] IsPropertyKey: Entry[21126]
[2714] IsPropertyKey: If[21127] (= (typeof argument) String)
[2715] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2716] OrdinaryGet: Normal[23776] assert (= __x0__ true)
[2717] OrdinaryGet: Call[23781] app __x1__ = (O.GetOwnProperty O P)
[2718] OrdinaryObject.GetOwnProperty: Entry[23863]
[2719] OrdinaryObject.GetOwnProperty: Call[23864] app __x0__ = (OrdinaryGetOwnProperty O P)
[2720] OrdinaryGetOwnProperty: Entry[23788]
[2721] OrdinaryGetOwnProperty: Call[23789] app __x0__ = (IsPropertyKey P)
[2722] IsPropertyKey: Entry[21126]
[2723] IsPropertyKey: If[21127] (= (typeof argument) String)
[2724] IsPropertyKey: Normal[21130] return true
<RETURN> true
[2725] OrdinaryGetOwnProperty: Normal[23795] assert (= __x0__ true)
[2726] OrdinaryGetOwnProperty: If[23799] (= O.SubMap[P] absent)
[2727] OrdinaryGetOwnProperty: Normal[23790] let D = (new PropertyDescriptor())
[2728] OrdinaryGetOwnProperty: Normal[23791] let X = O.SubMap[P]
[2729] OrdinaryGetOwnProperty: Call[23796] app __x1__ = (IsDataDescriptor X)
[2730] IsDataDescriptor: Entry[21031]
[2731] IsDataDescriptor: If[21032] (= Desc undefined)
[2732] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2733] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2734] OrdinaryGetOwnProperty: If[23803] __x1__
[2735] OrdinaryGetOwnProperty: Normal[23797] D.Value = X.Value
[2736] OrdinaryGetOwnProperty: Normal[23792] D.Writable = X.Writable
[2737] OrdinaryGetOwnProperty: Normal[23793] D.Enumerable = X.Enumerable
[2738] OrdinaryGetOwnProperty: Normal[23805] D.Configurable = X.Configurable
[2739] OrdinaryGetOwnProperty: Normal[23800] return D
<RETURN> #61 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> 3.0
  "Configurable" -> false
}
[2740] OrdinaryObject.GetOwnProperty: Normal[23865] return [! __x0__]
<RETURN> #61 -> (TYPE = PropertyDescriptor) {
  "Enumerable" -> true
  "Writable" -> true
  "Value" -> 3.0
  "Configurable" -> false
}
[2741] OrdinaryGet: Normal[23785] let desc = [? __x1__]
[2742] OrdinaryGet: If[23767] (= desc undefined)
[2743] OrdinaryGet: Call[23769] app __x4__ = (IsDataDescriptor desc)
[2744] IsDataDescriptor: Entry[21031]
[2745] IsDataDescriptor: If[21032] (= Desc undefined)
[2746] IsDataDescriptor: If[21036] (&& (= Desc.Value absent) (= Desc.Writable absent))
[2747] IsDataDescriptor: Normal[21033] return true
<RETURN> true
[2748] OrdinaryGet: If[23780] (= __x4__ true)
[2749] OrdinaryGet: Normal[23772] return desc.Value
<RETURN> 3.0
[2750] OrdinaryObject.Get: Normal[23861] return [? __x0__]
<RETURN> 3.0
[2751] Get: Normal[19224] return [? __x1__]
<RETURN> 3.0
[2752] ObjectEnvironmentRecord.GetBindingValue: Normal[23469] return [? __x1__]
<RETURN> 3.0
[2753] GlobalEnvironmentRecord.GetBindingValue: Normal[19823] return [? __x2__]
<RETURN> 3.0
[2754] GetValue: Normal[19560] return [? __x5__]
<RETURN> 3.0
[2755] ArgumentList[0,0].ArgumentListEvaluation: Normal[346] let arg = [? __x1__]
[2756] ArgumentList[0,0].ArgumentListEvaluation: Normal[347] return (new [arg])
<RETURN> #62 -> [3.0]
[2757] EvaluateCall: Normal[8229] let argList = [? __x3__]
[2758] EvaluateCall: If[8224] (! (= (typeof func) Object))
[2759] EvaluateCall: Call[8216] app __x4__ = (IsCallable func)
[2760] IsCallable: Entry[21002]
[2761] IsCallable: If[21003] (! (= (typeof argument) Object))
[2762] IsCallable: If[21007] (! (= argument.Call absent))
[2763] IsCallable: Normal[21008] return true
<RETURN> true
[2764] EvaluateCall: If[8233] (= __x4__ false)
[2765] EvaluateCall: If[8227] (= tailPosition true)
[2766] EvaluateCall: Call[8218] app __x6__ = (Call func thisValue argList)
[2767] Call: Entry[4062]
[2768] Call: If[4063] (= argumentsList absent)
[2769] Call: Call[4067] app __x0__ = (IsCallable F)
[2770] IsCallable: Entry[21002]
[2771] IsCallable: If[21003] (! (= (typeof argument) Object))
[2772] IsCallable: If[21007] (! (= argument.Call absent))
[2773] IsCallable: Normal[21008] return true
<RETURN> true
[2774] Call: If[4070] (= __x0__ false)
[2775] Call: Call[4065] app __x1__ = (F.Call F V argumentsList)
[2776] BuiltinFunctionObject.Call: Entry[3994]
[2777] BuiltinFunctionObject.Call: Normal[3995] let callerContext = CONTEXT
[2778] BuiltinFunctionObject.Call: If[4002] (= callerContext null)
[2779] BuiltinFunctionObject.Call: Normal[4007] let calleeContext = (new ExecutionContext())
[2780] BuiltinFunctionObject.Call: Normal[3996] calleeContext.Function = F
[2781] BuiltinFunctionObject.Call: Normal[3997] let calleeRealm = F.Realm
[2782] BuiltinFunctionObject.Call: Normal[4003] calleeContext.Realm = calleeRealm
[2783] BuiltinFunctionObject.Call: Normal[4009] calleeContext.ScriptOrModule = null
[2784] BuiltinFunctionObject.Call: Normal[4004] append calleeContext -> EXECUTION_STACK
[2785] BuiltinFunctionObject.Call: Normal[3998] CONTEXT = EXECUTION_STACK[(- EXECUTION_STACK.length 1i)]
[2786] BuiltinFunctionObject.Call: Call[3999] app result = (F.Code thisArgument argumentsList undefined)
[2787] GLOBAL.HostPrint: Entry[14241]
[2788] GLOBAL.HostPrint: Call[14242] app str = (GetArgument argumentsList)
[2789] GLOBAL.HostPrint: Normal[14243] print [? str]
3.0
[2790] GLOBAL.HostPrint: Normal[14244] return undefined
<RETURN> undefined
[2791] BuiltinFunctionObject.Call: If[4008] (= EXECUTION_STACK[(- EXECUTION_STACK.length 1i)] calleeContext)
[2792] BuiltinFunctionObject.Call: Normal[4005] (pop EXECUTION_STACK (- EXECUTION_STACK.length 1i))
[2793] BuiltinFunctionObject.Call: Normal[4000] CONTEXT = EXECUTION_STACK[(- EXECUTION_STACK.length 1i)]
[2794] BuiltinFunctionObject.Call: Normal[4001] return result
<RETURN> N(undefined)
[2795] Call: Normal[4068] return [? __x1__]
<RETURN> undefined
[2796] EvaluateCall: Normal[8222] let result = __x6__
[2797] EvaluateCall: Normal[8228] return result
<RETURN> N(undefined)
[2798] CallExpression[0,0].Evaluation: Normal[4097] return [? __x11__]
<RETURN> undefined
[2799] ExpressionStatement[0,0].Evaluation: Normal[8764] let exprRef = __x0__
[2800] ExpressionStatement[0,0].Evaluation: Call[8765] app __x1__ = (GetValue exprRef)
[2801] GetValue: Entry[19545]
[2802] GetValue: Normal[19546] [? V]
[2803] GetValue: If[19554] (! (is-instance-of V ReferenceRecord))
[2804] GetValue: Normal[19558] return V
<RETURN> undefined
[2805] ExpressionStatement[0,0].Evaluation: Normal[8761] return [? __x1__]
<RETURN> undefined
[2806] StatementList[1,0].Evaluation: Normal[26876] let s = __x1__
[2807] StatementList[1,0].Evaluation: Call[26877] app __x2__ = (UpdateEmpty s sl)
[2808] UpdateEmpty: Entry[28735]
[2809] UpdateEmpty: If[28736] (! (= completionRecord.Value ~empty~))
[2810] UpdateEmpty: Normal[28737] return completionRecord
<RETURN> N(undefined)
[2811] StatementList[1,0].Evaluation: Normal[26879] return __x2__
<RETURN> N(undefined)
[2812] ScriptEvaluation: Normal[26042] result = __x1__
[2813] ScriptEvaluation: If[26027] (&& (= result.Type ~normal~) (= result.Value ~empty~))
[2814] ScriptEvaluation: Normal[26028] CONTEXT = null
[2815] ScriptEvaluation: If[26029] (= EXECUTION_STACK[(- EXECUTION_STACK.length 1i)] scriptContext)
[2816] ScriptEvaluation: Normal[26032] (pop EXECUTION_STACK (- EXECUTION_STACK.length 1i))
[2817] ScriptEvaluation: Normal[26033] assert (< 0i EXECUTION_STACK.length)
[2818] ScriptEvaluation: Normal[26043] CONTEXT = EXECUTION_STACK[(- EXECUTION_STACK.length 1i)]
[2819] ScriptEvaluation: Normal[26044] return result
<RETURN> N(undefined)
[2820] ScriptEvaluationJob: Normal[26052] [? __x1__]
[2821] ScriptEvaluationJob: Normal[26048] return undefined
<RETURN> undefined
[2822] TOP_LEVEL: Normal[25932] let result = __x3__
[2823] TOP_LEVEL: Call[25943] app __x4__ = (IsAbruptCompletion result)
[2824] TOP_LEVEL: If[25939] __x4__
[2825] TOP_LEVEL: LoopCont[25941]
[2826] TOP_LEVEL: Loop[25926] true
[2827] TOP_LEVEL: If[25911] (= EXECUTION_STACK[(- EXECUTION_STACK.length 1i)] CONTEXT)
[2828] TOP_LEVEL: Normal[25912] let __x2__ = (- EXECUTION_STACK.length 1i)
[2829] TOP_LEVEL: Normal[25919] (pop EXECUTION_STACK __x2__)
[2830] TOP_LEVEL: If[25923] (= EXECUTION_STACK.length 0i)
[2831] TOP_LEVEL: Normal[25920] CONTEXT = null
[2832] TOP_LEVEL: If[25915] (= JOB_QUEUE.length 0.0)
[2833] TOP_LEVEL: Normal[25921] return undefined
<RETURN> undefined
{
  context: {
    name: TOP_LEVEL
    return: RETURN
    cursor: [EMPTY]
    local-vars: {
      newContext -> #22
      __x3__ -> N(undefined)
      job -> λ(ScriptEvaluationJob)
      __x0__ -> ~empty~
      __x1__ -> N(~empty~)
      __x2__ -> 0i
      RESULT -> N(undefined)
      __x4__ -> false
      args -> #20
      result -> N(undefined)
      nextQueue -> #JOB_QUEUE
      nextPending -> #21
    }
  }
  context-stack: []
  globals: {
    CreateListFromArrayLike -> λ(CreateListFromArrayLike)
    NumberToBigInt -> λ(NumberToBigInt)
    CreateAsyncFromSyncIterator -> λ(CreateAsyncFromSyncIterator)
    CreateAsyncIteratorFromClosure -> λ(CreateAsyncIteratorFromClosure)
    SCRIPT_BODY -> ☊[ScriptBody](var x = 1 + 2 ; print ( x ) ;)
    TypedArraySpeciesCreate -> λ(TypedArraySpeciesCreate)
    ResolveBinding -> λ(ResolveBinding)
    IsExtensible -> λ(IsExtensible)
    msFromTime -> λ(msFromTime)
    ToPrimitive -> λ(ToPrimitive)
    HoursPerDay -> λ(HoursPerDay)
    BigInt::bitwiseNOT -> λ(BigInt::bitwiseNOT)
    GetPromiseResolve -> λ(GetPromiseResolve)
    GetActiveScriptOrModule -> λ(GetActiveScriptOrModule)
    RegExpExec -> λ(RegExpExec)
    SetImmutablePrototype -> λ(SetImmutablePrototype)
    GeneratorResumeAbrupt -> λ(GeneratorResumeAbrupt)
    ImportedLocalNames -> λ(ImportedLocalNames)
    BigInt::add -> λ(BigInt::add)
    IsSuperReference -> λ(IsSuperReference)
    OrdinaryCreateFromConstructor -> λ(OrdinaryCreateFromConstructor)
    UTF16SurrogatePairToCodePoint -> λ(UTF16SurrogatePairToCodePoint)
    CreateIterResultObject -> λ(CreateIterResultObject)
    Get -> λ(Get)
    CreateByteDataBlock -> λ(CreateByteDataBlock)
    RegExpBuiltinExec -> λ(RegExpBuiltinExec)
    TypedArrayCreate -> λ(TypedArrayCreate)
    IsStringPrefix -> λ(IsStringPrefix)
    OrdinaryIsExtensible -> λ(OrdinaryIsExtensible)
    AddToKeptObjects -> λ(AddToKeptObjects)
    JOB_QUEUE -> #JOB_QUEUE
    TestIntegrityLevel -> λ(TestIntegrityLevel)
    ToPropertyDescriptor -> λ(ToPropertyDescriptor)
    BigInt::sameValue -> λ(BigInt::sameValue)
    MakeConstructor -> λ(MakeConstructor)
    NewFunctionEnvironment -> λ(NewFunctionEnvironment)
    GlobalDeclarationInstantiation -> λ(GlobalDeclarationInstantiation)
    MakeArgSetter -> λ(MakeArgSetter)
    Evaluate -> λ(Evaluate)
    GetV -> λ(GetV)
    Undefined -> "Undefined"
    UTF16EncodeCodePoint -> λ(UTF16EncodeCodePoint)
    CONTEXT -> null
    CleanupFinalizationRegistry -> λ(CleanupFinalizationRegistry)
    ToPropertyKey -> λ(ToPropertyKey)
    EnumerableOwnPropertyNames -> λ(EnumerableOwnPropertyNames)
    SetFunctionName -> λ(SetFunctionName)
    IsConstructor -> λ(IsConstructor)
    NewPromiseReactionJob -> λ(NewPromiseReactionJob)
    Number::divide -> λ(Number::divide)
    IsValidIntegerIndex -> λ(IsValidIntegerIndex)
    IteratorValue -> λ(IteratorValue)
    IteratorClose -> λ(IteratorClose)
    Number -> "Number"
    SetViewValue -> λ(SetViewValue)
    GetValueFromBuffer -> λ(GetValueFromBuffer)
    ModuleNamespaceCreate -> λ(ModuleNamespaceCreate)
    AddEntriesFromIterable -> λ(AddEntriesFromIterable)
    OrdinaryToPrimitive -> λ(OrdinaryToPrimitive)
    NewModuleEnvironment -> λ(NewModuleEnvironment)
    CreateMappedArgumentsObject -> λ(CreateMappedArgumentsObject)
    CreateMethodProperty -> λ(CreateMethodProperty)
    ClearKeptObjects -> λ(ClearKeptObjects)
    GetIterator -> λ(GetIterator)
    SameValueZero -> λ(SameValueZero)
    CreateRealm -> λ(CreateRealm)
    RepeatMatcher -> λ(RepeatMatcher)
    GetWaiterList -> λ(GetWaiterList)
    OrdinaryGetOwnProperty -> λ(OrdinaryGetOwnProperty)
    SetValueInBuffer -> λ(SetValueInBuffer)
    PerformPromiseAny -> λ(PerformPromiseAny)
    IsWordChar -> λ(IsWordChar)
    IsSharedArrayBuffer -> λ(IsSharedArrayBuffer)
    SYMBOL_unscopables -> #GLOBAL.Symbol.unscopables
    IsArray -> λ(IsArray)
    ValidateTypedArray -> λ(ValidateTypedArray)
    StringToCodePoints -> λ(StringToCodePoints)
    GetGlobalObject -> λ(GetGlobalObject)
    SecondsPerMinute -> λ(SecondsPerMinute)
    Races -> λ(Races)
    PerformPromiseAllSettled -> λ(PerformPromiseAllSettled)
    ResolveThisBinding -> λ(ResolveThisBinding)
    AgentSignifier -> λ(AgentSignifier)
    IsDetachedBuffer -> λ(IsDetachedBuffer)
    Object -> "Object"
    InitializeReferencedBinding -> λ(InitializeReferencedBinding)
    CreateIteratorFromClosure -> λ(CreateIteratorFromClosure)
    GeneratorValidate -> λ(GeneratorValidate)
    SetTypedArrayFromArrayLike -> λ(SetTypedArrayFromArrayLike)
    InitializeEnvironment -> λ(InitializeEnvironment)
    PRIMITIVE -> #PRIMITIVE
    ForInOfBodyEvaluation -> λ(ForInOfBodyEvaluation)
    SYMBOL_replace -> #GLOBAL.Symbol.replace
    Number::multiply -> λ(Number::multiply)
    AsyncGeneratorResumeNext -> λ(AsyncGeneratorResumeNext)
    MakeDate -> λ(MakeDate)
    thisBooleanValue -> λ(thisBooleanValue)
    AllocateSharedArrayBuffer -> λ(AllocateSharedArrayBuffer)
    HostMakeJobCallback -> λ(HostMakeJobCallback)
    ToUint16 -> λ(ToUint16)
    AsyncGeneratorValidate -> λ(AsyncGeneratorValidate)
    AddWaiter -> λ(AddWaiter)
    ToLength -> λ(ToLength)
    FlattenIntoArray -> λ(FlattenIntoArray)
    IsGenericDescriptor -> λ(IsGenericDescriptor)
    OrdinaryCallEvaluateBody -> λ(OrdinaryCallEvaluateBody)
    SortCompare -> λ(SortCompare)
    SYMBOL_match -> #GLOBAL.Symbol.match
    IteratorComplete -> λ(IteratorComplete)
    CompletePropertyDescriptor -> λ(CompletePropertyDescriptor)
    OrdinaryDefineOwnProperty -> λ(OrdinaryDefineOwnProperty)
    TimeFromYear -> λ(TimeFromYear)
    GetNewTarget -> λ(GetNewTarget)
    Await -> λ(Await)
    AllocateTypedArray -> λ(AllocateTypedArray)
    SpeciesConstructor -> λ(SpeciesConstructor)
    GetExportedNames -> λ(GetExportedNames)
    Number::toString -> λ(Number::toString)
    GeneratorYield -> λ(GeneratorYield)
    ModuleRecord.ResolveExport -> λ(ModuleRecord.ResolveExport)
    EvaluatePropertyAccessWithExpressionKey -> λ(EvaluatePropertyAccessWithExpressionKey)
    BigInt::sameValueZero -> λ(BigInt::sameValueZero)
    CreateSharedByteDataBlock -> λ(CreateSharedByteDataBlock)
    SymbolDescriptiveString -> λ(SymbolDescriptiveString)
    OrdinarySet -> λ(OrdinarySet)
    CreateDynamicFunction -> λ(CreateDynamicFunction)
    HostGetImportMetaProperties -> λ(HostGetImportMetaProperties)
    AbstractRelationalComparison -> λ(AbstractRelationalComparison)
    HasProperty -> λ(HasProperty)
    OrdinarySetPrototypeOf -> λ(OrdinarySetPrototypeOf)
    SetIntegrityLevel -> λ(SetIntegrityLevel)
    BigInt::unsignedRightShift -> λ(BigInt::unsignedRightShift)
    CreateIntrinsics -> λ(CreateIntrinsics)
    ComposeWriteEventBytes -> λ(ComposeWriteEventBytes)
    CopyDataProperties -> λ(CopyDataProperties)
    UnicodeMatchPropertyValue -> λ(UnicodeMatchPropertyValue)
    CreateListIteratorRecord -> λ(CreateListIteratorRecord)
    UTC -> λ(UTC)
    CreateArrayFromList -> λ(CreateArrayFromList)
    Construct -> λ(Construct)
    EXECUTION_STACK -> #EXECUTION_STACK
    msPerHour -> λ(msPerHour)
    Canonicalize -> λ(Canonicalize)
    DetachArrayBuffer -> λ(DetachArrayBuffer)
    WeekDay -> λ(WeekDay)
    MakeSuperPropertyReference -> λ(MakeSuperPropertyReference)
    UpdateEmpty -> λ(UpdateEmpty)
    CloneArrayBuffer -> λ(CloneArrayBuffer)
    BinaryAnd -> λ(BinaryAnd)
    IteratorStep -> λ(IteratorStep)
    LengthOfArrayLike -> λ(LengthOfArrayLike)
    ToDateString -> λ(ToDateString)
    EscapeRegExpPattern -> λ(EscapeRegExpPattern)
    AllocateArrayBuffer -> λ(AllocateArrayBuffer)
    CoherentReads -> λ(CoherentReads)
    thisStringValue -> λ(thisStringValue)
    ToNumeric -> λ(ToNumeric)
    ToInt32 -> λ(ToInt32)
    AtomicReadModifyWrite -> λ(AtomicReadModifyWrite)
    BigInt::exponentiate -> λ(BigInt::exponentiate)
    CopyDataBlockBytes -> λ(CopyDataBlockBytes)
    StringIndexOf -> λ(StringIndexOf)
    ParseScript -> λ(ParseScript)
    CreateBuiltinFunction -> λ(CreateBuiltinFunction)
    Boolean -> "Boolean"
    EnqueueJob -> λ(EnqueueJob)
    AsyncGeneratorYield -> λ(AsyncGeneratorYield)
    StringToBigInt -> λ(StringToBigInt)
    ToBigInt -> λ(ToBigInt)
    DayFromYear -> λ(DayFromYear)
    FunctionDeclarationInstantiation -> λ(FunctionDeclarationInstantiation)
    OrdinaryObjectCreate -> λ(OrdinaryObjectCreate)
    EvaluatePropertyAccessWithIdentifierKey -> λ(EvaluatePropertyAccessWithIdentifierKey)
    InstanceofOperator -> λ(InstanceofOperator)
    ArraySpeciesCreate -> λ(ArraySpeciesCreate)
    CanonicalNumericIndexString -> λ(CanonicalNumericIndexString)
    OrdinaryPreventExtensions -> λ(OrdinaryPreventExtensions)
    ForBodyEvaluation -> λ(ForBodyEvaluation)
    DeletePropertyOrThrow -> λ(DeletePropertyOrThrow)
    NotifyWaiter -> λ(NotifyWaiter)
    IsPromise -> λ(IsPromise)
    GetFunctionRealm -> λ(GetFunctionRealm)
    Number::leftShift -> λ(Number::leftShift)
    SYMBOL_hasInstance -> #GLOBAL.Symbol.hasInstance
    HostEventSet -> λ(HostEventSet)
    Number::sameValueZero -> λ(Number::sameValueZero)
    CodePointsToString -> λ(CodePointsToString)
    AgentCanSuspend -> λ(AgentCanSuspend)
    IsLabelledFunction -> λ(IsLabelledFunction)
    CreatePerIterationEnvironment -> λ(CreatePerIterationEnvironment)
    ToBoolean -> λ(ToBoolean)
    Call -> λ(Call)
    HasOwnProperty -> λ(HasOwnProperty)
    OrdinaryGet -> λ(OrdinaryGet)
    Number::signedRightShift -> λ(Number::signedRightShift)
    OrdinaryOwnPropertyKeys -> λ(OrdinaryOwnPropertyKeys)
    msPerMinute -> λ(msPerMinute)
    EvalDeclarationInstantiation -> λ(EvalDeclarationInstantiation)
    MonthFromTime -> λ(MonthFromTime)
    ByteListBitwiseOp -> λ(ByteListBitwiseOp)
    MakeClassConstructor -> λ(MakeClassConstructor)
    SetFunctionLength -> λ(SetFunctionLength)
    PutValue -> λ(PutValue)
    IsUnresolvableReference -> λ(IsUnresolvableReference)
    StringGetOwnProperty -> λ(StringGetOwnProperty)
    SerializeJSONProperty -> λ(SerializeJSONProperty)
    EnterCriticalSection -> λ(EnterCriticalSection)
    InnerModuleLinking -> λ(InnerModuleLinking)
    ValueOfReadEvent -> λ(ValueOfReadEvent)
    ArraySetLength -> λ(ArraySetLength)
    HOST_DEFINED -> undefined
    StringCreate -> λ(StringCreate)
    HostEnsureCanCompileStrings -> λ(HostEnsureCanCompileStrings)
    Number::subtract -> λ(Number::subtract)
    SYMBOL_asyncIterator -> #GLOBAL.Symbol.asyncIterator
    GetMethod -> λ(GetMethod)
    AsyncGeneratorReject -> λ(AsyncGeneratorReject)
    SYMBOL_matchAll -> #GLOBAL.Symbol.matchAll
    OrdinaryFunctionCreate -> λ(OrdinaryFunctionCreate)
    TimeWithinDay -> λ(TimeWithinDay)
    ProxyRevocationFunctions -> λ(ProxyRevocationFunctions)
    TheAbstractClosureSpecificationType -> λ(TheAbstractClosureSpecificationType)
    Decode -> λ(Decode)
    InitializeHostDefinedRealm -> λ(InitializeHostDefinedRealm)
    CreateRegExpStringIterator -> λ(CreateRegExpStringIterator)
    GetTemplateObject -> λ(GetTemplateObject)
    msPerSecond -> λ(msPerSecond)
    ToInt8 -> λ(ToInt8)
    thisBigIntValue -> λ(thisBigIntValue)
    %TypedArray%.prototype.sort -> λ(%TypedArray%.prototype.sort)
    IntegerIndexedElementGet -> λ(IntegerIndexedElementGet)
    RegExpInitialize -> λ(RegExpInitialize)
    String -> "String"
    ParsePattern -> λ(ParsePattern)
    ForInOfHeadEvaluation -> λ(ForInOfHeadEvaluation)
    ToUint8Clamp -> λ(ToUint8Clamp)
    HostEnqueuePromiseJob -> λ(HostEnqueuePromiseJob)
    NewPromiseCapability -> λ(NewPromiseCapability)
    BoundFunctionCreate -> λ(BoundFunctionCreate)
    TimeZoneString -> λ(TimeZoneString)
    ApplyStringOrNumericBinaryOperator -> λ(ApplyStringOrNumericBinaryOperator)
    AsyncFromSyncIteratorContinuation -> λ(AsyncFromSyncIteratorContinuation)
    IsCompatiblePropertyDescriptor -> λ(IsCompatiblePropertyDescriptor)
    TearFreeReads -> λ(TearFreeReads)
    ToBigInt64 -> λ(ToBigInt64)
    BinaryXor -> λ(BinaryXor)
    AsyncGeneratorEnqueue -> λ(AsyncGeneratorEnqueue)
    UnicodeMatchProperty -> λ(UnicodeMatchProperty)
    IsRegExp -> λ(IsRegExp)
    AsyncGeneratorStart -> λ(AsyncGeneratorStart)
    GLOBAL -> #GLOBAL
    Number::remainder -> λ(Number::remainder)
    ValidateIntegerTypedArray -> λ(ValidateIntegerTypedArray)
    ToIndex -> λ(ToIndex)
    NewObjectEnvironment -> λ(NewObjectEnvironment)
    TimeString -> λ(TimeString)
    RemoveWaiters -> λ(RemoveWaiters)
    InitializeBoundName -> λ(InitializeBoundName)
    CreateResolvingFunctions -> λ(CreateResolvingFunctions)
    IsConcatSpreadable -> λ(IsConcatSpreadable)
    PerformEval -> λ(PerformEval)
    GetIdentifierReference -> λ(GetIdentifierReference)
    LoopContinues -> λ(LoopContinues)
    RawBytesToNumeric -> λ(RawBytesToNumeric)
    ToBigUint64 -> λ(ToBigUint64)
    InitializeTypedArrayFromTypedArray -> λ(InitializeTypedArrayFromTypedArray)
    BigIntBitwiseOp -> λ(BigIntBitwiseOp)
    SameValueNonNumeric -> λ(SameValueNonNumeric)
    SYMBOL_toPrimitive -> #GLOBAL.Symbol.toPrimitive
    SYMBOL_search -> #GLOBAL.Symbol.search
    RemoveWaiter -> λ(RemoveWaiter)
    BigInt::toString -> λ(BigInt::toString)
    IsValidRegularExpressionLiteral -> λ(IsValidRegularExpressionLiteral)
    msPerDay -> λ(msPerDay)
    SetDefaultGlobalBindings -> λ(SetDefaultGlobalBindings)
    TrimString -> λ(TrimString)
    FinishDynamicImport -> λ(FinishDynamicImport)
    ToNumber -> λ(ToNumber)
    SerializeJSONArray -> λ(SerializeJSONArray)
    StringPad -> λ(StringPad)
    BinaryOr -> λ(BinaryOr)
    CharacterSetMatcher -> λ(CharacterSetMatcher)
    FromPropertyDescriptor -> λ(FromPropertyDescriptor)
    HostFinalizeImportMeta -> λ(HostFinalizeImportMeta)
    Contains -> λ(Contains)
    SYMBOL_iterator -> #GLOBAL.Symbol.iterator
    PromiseResolve -> λ(PromiseResolve)
    RunJobs -> λ(RunJobs)
    IntegerIndexedObjectCreate -> λ(IntegerIndexedObjectCreate)
    RequireObjectCoercible -> λ(RequireObjectCoercible)
    Number::bitwiseAND -> λ(Number::bitwiseAND)
    ModuleRecord.Link -> λ(ModuleRecord.Link)
    ValidateAndApplyPropertyDescriptor -> λ(ValidateAndApplyPropertyDescriptor)
    ScriptEvaluationJob -> λ(ScriptEvaluationJob)
    PerformPromiseThen -> λ(PerformPromiseThen)
    ToString -> λ(ToString)
    Number::sameValue -> λ(Number::sameValue)
    BigInt::leftShift -> λ(BigInt::leftShift)
    GetModuleNamespace -> λ(GetModuleNamespace)
    ToIntegerOrInfinity -> λ(ToIntegerOrInfinity)
    SharedDataBlockEventSet -> λ(SharedDataBlockEventSet)
    Number::lessThan -> λ(Number::lessThan)
    InitializeTypedArrayFromArrayBuffer -> λ(InitializeTypedArrayFromArrayBuffer)
    MinFromTime -> λ(MinFromTime)
    MakeArgGetter -> λ(MakeArgGetter)
    NormalCompletion -> λ(NormalCompletion)
    CreateUnmappedArgumentsObject -> λ(CreateUnmappedArgumentsObject)
    InLeapYear -> λ(InLeapYear)
    SYMBOL_REGISTRY -> #SYMBOL_REGISTRY
    CreateArrayIterator -> λ(CreateArrayIterator)
    IsNoTearConfiguration -> λ(IsNoTearConfiguration)
    PrepareForTailCall -> λ(PrepareForTailCall)
    LocalTime -> λ(LocalTime)
    BigInt::subtract -> λ(BigInt::subtract)
    GeneratorStart -> λ(GeneratorStart)
    CharacterRange -> λ(CharacterRange)
    EnumerateObjectProperties -> λ(EnumerateObjectProperties)
    GetThisEnvironment -> λ(GetThisEnvironment)
    ValidateAtomicAccess -> λ(ValidateAtomicAccess)
    ThrowCompletion -> λ(ThrowCompletion)
    ALGORITHM -> #ALGORITHM
    Number::add -> λ(Number::add)
    ToUint8 -> λ(ToUint8)
    BigInt::unaryMinus -> λ(BigInt::unaryMinus)
    GetThisValue -> λ(GetThisValue)
    TriggerPromiseReactions -> λ(TriggerPromiseReactions)
    ByteListEqual -> λ(ByteListEqual)
    Set -> λ(Set)
    GetViewValue -> λ(GetViewValue)
    SetTypedArrayFromTypedArray -> λ(SetTypedArrayFromTypedArray)
    thisSymbolValue -> λ(thisSymbolValue)
    ArrayCreate -> λ(ArrayCreate)
    ScriptEvaluation -> λ(ScriptEvaluation)
    BigInt::equal -> λ(BigInt::equal)
    RegExpCreate -> λ(RegExpCreate)
    ValidChosenReads -> λ(ValidChosenReads)
    IterableToList -> λ(IterableToList)
    BigInt::divide -> λ(BigInt::divide)
    Number::unsignedRightShift -> λ(Number::unsignedRightShift)
    IsUnsignedElementType -> λ(IsUnsignedElementType)
    ToUint32 -> λ(ToUint32)
    RegExpAlloc -> λ(RegExpAlloc)
    BigInt::signedRightShift -> λ(BigInt::signedRightShift)
    Number::equal -> λ(Number::equal)
    ParseModule -> λ(ParseModule)
    AdvanceStringIndex -> λ(AdvanceStringIndex)
    DaysInYear -> λ(DaysInYear)
    EventSet -> λ(EventSet)
    SYMBOL_species -> #GLOBAL.Symbol.species
    GetGeneratorKind -> λ(GetGeneratorKind)
    LeaveCriticalSection -> λ(LeaveCriticalSection)
    NewPromiseResolveThenableJob -> λ(NewPromiseResolveThenableJob)
    IsAnonymousFunctionDefinition -> λ(IsAnonymousFunctionDefinition)
    IsInTailPosition -> λ(IsInTailPosition)
    OrdinarySetWithOwnDescriptor -> λ(OrdinarySetWithOwnDescriptor)
    BackreferenceMatcher -> λ(BackreferenceMatcher)
    GeneratorResume -> λ(GeneratorResume)
    Invoke -> λ(Invoke)
    BigInt::remainder -> λ(BigInt::remainder)
    GetSuperConstructor -> λ(GetSuperConstructor)
    DefinePropertyOrThrow -> λ(DefinePropertyOrThrow)
    SYMBOL_toStringTag -> #GLOBAL.Symbol.toStringTag
    SecFromTime -> λ(SecFromTime)
    Null -> "Null"
    AbstractEqualityComparison -> λ(AbstractEqualityComparison)
    PrepareForOrdinaryCall -> λ(PrepareForOrdinaryCall)
    Link -> λ(Link)
    FulfillPromise -> λ(FulfillPromise)
    ProxyCreate -> λ(ProxyCreate)
    CreateSetIterator -> λ(CreateSetIterator)
    GetSubstitution -> λ(GetSubstitution)
    OrdinaryDelete -> λ(OrdinaryDelete)
    INTRINSICS -> #INTRINSICS
    CaseClauseIsSelected -> λ(CaseClauseIsSelected)
    EvaluateNew -> λ(EvaluateNew)
    OrdinaryGetPrototypeOf -> λ(OrdinaryGetPrototypeOf)
    IsIntegralNumber -> λ(IsIntegralNumber)
    InitializeTypedArrayFromArrayLike -> λ(InitializeTypedArrayFromArrayLike)
    SYMBOL_isConcatSpreadable -> #GLOBAL.Symbol.isConcatSpreadable
    thisTimeValue -> λ(thisTimeValue)
    EvaluateCall -> λ(EvaluateCall)
    ObjectDefineProperties -> λ(ObjectDefineProperties)
    InitializeTypedArrayFromList -> λ(InitializeTypedArrayFromList)
    BigInt::bitwiseXOR -> λ(BigInt::bitwiseXOR)
    MinutesPerHour -> λ(MinutesPerHour)
    MakeMethod -> λ(MakeMethod)
    CreateDataProperty -> λ(CreateDataProperty)
    DateFromTime -> λ(DateFromTime)
    NewDeclarativeEnvironment -> λ(NewDeclarativeEnvironment)
    Number::bitwiseOR -> λ(Number::bitwiseOR)
    StrictEqualityComparison -> λ(StrictEqualityComparison)
    BigInt::multiply -> λ(BigInt::multiply)
    EarlyErrors -> λ(EarlyErrors)
    GetModifySetValueInBuffer -> λ(GetModifySetValueInBuffer)
    Symbol -> "Symbol"
    HostPromiseRejectionTracker -> λ(HostPromiseRejectionTracker)
    AllocateTypedArrayBuffer -> λ(AllocateTypedArrayBuffer)
    SYMBOL_split -> #GLOBAL.Symbol.split
    BigInt::lessThan -> λ(BigInt::lessThan)
    REALM -> #REALM
    IsBigIntElementType -> λ(IsBigIntElementType)
    OrdinaryCallBindThis -> λ(OrdinaryCallBindThis)
    BigInt::bitwiseOR -> λ(BigInt::bitwiseOR)
    ToInt16 -> λ(ToInt16)
    AsyncGeneratorResolve -> λ(AsyncGeneratorResolve)
    ToObject -> λ(ToObject)
    NumericToRawBytes -> λ(NumericToRawBytes)
    RET_CONT -> undefined
    thisNumberValue -> λ(thisNumberValue)
    WeakRefDeref -> λ(WeakRefDeref)
    IteratorNext -> λ(IteratorNext)
    CreateForInIterator -> λ(CreateForInIterator)
    OrdinaryHasInstance -> λ(OrdinaryHasInstance)
    RejectPromise -> λ(RejectPromise)
    NewGlobalEnvironment -> λ(NewGlobalEnvironment)
    YearFromTime -> λ(YearFromTime)
    BigInt -> "BigInt"
    Number::bitwiseXOR -> λ(Number::bitwiseXOR)
    Number::exponentiate -> λ(Number::exponentiate)
    IsUnclampedIntegerElementType -> λ(IsUnclampedIntegerElementType)
    DataRaces -> λ(DataRaces)
    ResolveExport -> λ(ResolveExport)
    RequireInternalSlot -> λ(RequireInternalSlot)
    IsDataDescriptor -> λ(IsDataDescriptor)
    HourFromTime -> λ(HourFromTime)
    SetRealmGlobalObject -> λ(SetRealmGlobalObject)
    ModuleRecord.Evaluate -> λ(ModuleRecord.Evaluate)
    NumberBitwiseOp -> λ(NumberBitwiseOp)
    PerformPromiseAll -> λ(PerformPromiseAll)
    GetPrototypeFromConstructor -> λ(GetPrototypeFromConstructor)
    AsyncFunctionStart -> λ(AsyncFunctionStart)
    EvaluateStringOrNumericBinaryExpression -> λ(EvaluateStringOrNumericBinaryExpression)
    AsyncIteratorClose -> λ(AsyncIteratorClose)
    BigInt::bitwiseAND -> λ(BigInt::bitwiseAND)
    Day -> λ(Day)
    HostCallJobCallback -> λ(HostCallJobCallback)
    DayWithinYear -> λ(DayWithinYear)
    IsPropertyKey -> λ(IsPropertyKey)
    CreateDataPropertyOrThrow -> λ(CreateDataPropertyOrThrow)
    AddRestrictedFunctionProperties -> λ(AddRestrictedFunctionProperties)
    MakeBasicObject -> λ(MakeBasicObject)
    CreateMapIterator -> λ(CreateMapIterator)
    DateString -> λ(DateString)
    CodePointAt -> λ(CodePointAt)
    Yield -> λ(Yield)
    IntegerIndexedElementSet -> λ(IntegerIndexedElementSet)
    Execution -> λ(Execution)
    Number::bitwiseNOT -> λ(Number::bitwiseNOT)
    IsCallable -> λ(IsCallable)
    SuspendAgent -> λ(SuspendAgent)
    TimeClip -> λ(TimeClip)
    Encode -> λ(Encode)
    BlockDeclarationInstantiation -> λ(BlockDeclarationInstantiation)
    GetOwnPropertyKeys -> λ(GetOwnPropertyKeys)
    SplitMatch -> λ(SplitMatch)
    PerformPromiseRace -> λ(PerformPromiseRace)
    ParseText -> λ(ParseText)
    SameValue -> λ(SameValue)
    Number::unaryMinus -> λ(Number::unaryMinus)
    Reference -> "Reference"
    UnicodeEscape -> λ(UnicodeEscape)
    MakeDay -> λ(MakeDay)
    GetValue -> λ(GetValue)
    QuoteJSONString -> λ(QuoteJSONString)
    MakeTime -> λ(MakeTime)
    IsPropertyReference -> λ(IsPropertyReference)
    SerializeJSONObject -> λ(SerializeJSONObject)
    InnerModuleEvaluation -> λ(InnerModuleEvaluation)
    NumberToString -> λ(NumberToString)
    OrdinaryHasProperty -> λ(OrdinaryHasProperty)
    IsAccessorDescriptor -> λ(IsAccessorDescriptor)
    HostImportModuleDynamically -> λ(HostImportModuleDynamically)
    ExecuteModule -> λ(ExecuteModule)
  }
  heap: (SIZE = 64): {
    #GLOBAL.Object.getOwnPropertySymbols -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "getOwnPropertySymbols"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.getOwnPropertySymbols.SubMap
      "Code" -> λ(GLOBAL.Object.getOwnPropertySymbols)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.isFrozen -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.isFrozen
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.allSettled.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "allSettled"
      "Configurable" -> true
    }
    #DESC:GLOBAL.SetIteratorPrototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Number.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakSet.prototype.delete -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakSet.prototype.delete
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.keys.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.keys.name
      "length" -> #DESC:GLOBAL.Map.prototype.keys.length
    }
    #DESC:GLOBAL.String.prototype.valueOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.valueOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.SyntaxError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.SyntaxError.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.EvalError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.EvalError.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncGenerator.prototype.next
      "Configurable" -> true
    }
    #GLOBAL.IteratorPrototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.iterator -> #DESC:GLOBAL.IteratorPrototype[SYMBOL_iterator]
    }
    #DESC:GLOBAL.Map.prototype.values.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.slice.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncFromSyncIteratorPrototype.next
      "Configurable" -> true
    }
    #GLOBAL.Error -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Error"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Error.SubMap
      "Code" -> λ(GLOBAL.Error)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.DefaultConstructorFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "DefaultConstructorFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.DefaultConstructorFunctions.SubMap
      "Code" -> λ(GLOBAL.DefaultConstructorFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ArrayIteratorPrototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ArrayIteratorPrototype.next
      "Configurable" -> true
    }
    #DESC:GLOBAL.Error.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.match.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.match.name
      "length" -> #DESC:GLOBAL.String.prototype.match.length
    }
    #GLOBAL.Set[SYMBOL_species].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set[SYMBOL_species].name
      "length" -> #DESC:GLOBAL.Set[SYMBOL_species].length
    }
    #27 -> []
    #20 -> [☊[ScriptBody](var x = 1 + 2 ; print ( x ) ;), undefined]
    #DESC:GLOBAL.DefaultConstructorFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.DefaultConstructorFunctions
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.delete -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "delete"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.delete.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.delete)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.shift -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "shift"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.shift.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.shift)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.NaN -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> NaN
      "Configurable" -> false
    }
    #DESC:GLOBAL.Set.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Set"
      "Configurable" -> true
    }
    #GLOBAL.Array.isArray -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isArray"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.isArray.SubMap
      "Code" -> λ(GLOBAL.Array.isArray)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype[SYMBOL_iterator].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype[SYMBOL_iterator].name
      "length" -> #DESC:GLOBAL.String.prototype[SYMBOL_iterator].length
    }
    #GLOBAL.ReferenceError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ReferenceError.prototype.name
      "constructor" -> #DESC:GLOBAL.ReferenceError.prototype.constructor
      "message" -> #DESC:GLOBAL.ReferenceError.prototype.message
    }
    #GLOBAL.Number.isNaN.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.isNaN.name
      "length" -> #DESC:GLOBAL.Number.isNaN.length
    }
    #GLOBAL.String.prototype.match -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "match"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.match.SubMap
      "Code" -> λ(GLOBAL.String.prototype.match)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.resolve.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.isFinite.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].keys -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.toLowerCase.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.String.fromCodePoint -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "fromCodePoint"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.fromCodePoint.SubMap
      "Code" -> λ(GLOBAL.String.fromCodePoint)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.includes.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "includes"
      "Configurable" -> true
    }
    #GLOBAL.Map.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.species -> #DESC:GLOBAL.Map[SYMBOL_species]
      "prototype" -> #DESC:GLOBAL.Map.prototype
      "name" -> #DESC:GLOBAL.Map.name
      "length" -> #DESC:GLOBAL.Map.length
    }
    #GLOBAL.__ABS__.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.__ABS__.name
      "length" -> #DESC:GLOBAL.__ABS__.length
    }
    #GLOBAL.String.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.String.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.GeneratorFunction.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "GeneratorFunction"
      "Configurable" -> true
    }
    #GLOBAL.URIError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "URIError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.URIError.SubMap
      "Code" -> λ(GLOBAL.URIError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map.prototype.has -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "has"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.has.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.has)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.GetCapabilitiesExecutorFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "GetCapabilitiesExecutorFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.GetCapabilitiesExecutorFunctions.SubMap
      "Code" -> λ(GLOBAL.GetCapabilitiesExecutorFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.getOwnPropertyDescriptor -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "getOwnPropertyDescriptor"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.getOwnPropertyDescriptor.SubMap
      "Code" -> λ(GLOBAL.Object.getOwnPropertyDescriptor)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.startsWith.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "startsWith"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.toLocaleUpperCase.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toLocaleUpperCase"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.reverse -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "reverse"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.reverse.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.reverse)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.toUpperCase -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.toUpperCase
      "Configurable" -> true
    }
    #GLOBAL.GetCapabilitiesExecutorFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.GetCapabilitiesExecutorFunctions.name
      "length" -> #DESC:GLOBAL.GetCapabilitiesExecutorFunctions.length
    }
    #GLOBAL.Array.prototype[SYMBOL_unscopables] -> (TYPE = OrdinaryObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> null
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.unscopables]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "SubMap" -> #GLOBAL.Array.prototype[SYMBOL_unscopables].SubMap
      "Code" -> λ(GLOBAL.Array.prototype[SYMBOL_unscopables])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map.prototype.get -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.get.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.get)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.BigInt.prototype.valueOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #PRIMITIVE.Number -> (TYPE = Record) {
      "toString" -> λ(Number::toString)
      "leftShift" -> λ(Number::leftShift)
      "bitwiseXOR" -> λ(Number::bitwiseXOR)
      "exponentiate" -> λ(Number::exponentiate)
      "unsignedRightShift" -> λ(Number::unsignedRightShift)
      "bitwiseNOT" -> λ(Number::bitwiseNOT)
      "lessThan" -> λ(Number::lessThan)
      "remainder" -> λ(Number::remainder)
      "unit" -> 1.0
      "bitwiseOR" -> λ(Number::bitwiseOR)
      "unaryMinus" -> λ(Number::unaryMinus)
      "divide" -> λ(Number::divide)
      "sameValueZero" -> λ(Number::sameValueZero)
      "equal" -> λ(Number::equal)
      "bitwiseAND" -> λ(Number::bitwiseAND)
      "multiply" -> λ(Number::multiply)
      "add" -> λ(Number::add)
      "signedRightShift" -> λ(Number::signedRightShift)
      "subtract" -> λ(Number::subtract)
      "sameValue" -> λ(Number::sameValue)
    }
    #GLOBAL.String.prototype.includes.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.includes.name
      "length" -> #DESC:GLOBAL.String.prototype.includes.length
    }
    #GLOBAL.Array.prototype.flat.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.flat.name
      "length" -> #DESC:GLOBAL.Array.prototype.flat.length
    }
    #DESC:GLOBAL.Object.isExtensible.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.create.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "create"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype[SYMBOL_toPrimitive].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.toPrimitive]"
      "Configurable" -> true
    }
    #GLOBAL.Symbol.REGISTRY -> (Symbol "Symbol.REGISTRY")
    #DESC:GLOBAL.encodeURI -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.encodeURI
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.pop -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.pop
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.NEGATIVE_INFINITY -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> -Infinity
      "Configurable" -> false
    }
    #GLOBAL.String.prototype.lastIndexOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "lastIndexOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.lastIndexOf.SubMap
      "Code" -> λ(GLOBAL.String.prototype.lastIndexOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.from.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.from.name
      "length" -> #DESC:GLOBAL.Array.from.length
    }
    #DESC:GLOBAL.Array.prototype.flatMap.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "flatMap"
      "Configurable" -> true
    }
    #52 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #GLOBAL.Array.prototype.entries -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "entries"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.entries.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.entries)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.push -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "push"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.push.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.push)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.__ABS__.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "__ABS__"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ForInIteratorPrototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.sort.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "sort"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.entries.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.MapIteratorPrototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.MapIteratorPrototype.next.SubMap
      "Code" -> λ(GLOBAL.MapIteratorPrototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ReferenceError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ReferenceError
      "Configurable" -> true
    }
    #45 -> ["Value"]
    #DESC:GLOBAL.WeakSet.prototype.has.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.prototype.valueOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "valueOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.isSealed.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isSealed"
      "Configurable" -> true
    }
    #GLOBAL.Number.isInteger -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isInteger"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.isInteger.SubMap
      "Code" -> λ(GLOBAL.Number.isInteger)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.TypedArray.of -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "of"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.TypedArray.of.SubMap
      "Code" -> λ(GLOBAL.TypedArray.of)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.IteratorPrototype[SYMBOL_iterator] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.IteratorPrototype[SYMBOL_iterator]
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype.description.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Symbol.prototype.description.name
      "length" -> #DESC:GLOBAL.Symbol.prototype.description.length
    }
    #GLOBAL.WeakMap.prototype.get -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakMap.prototype.get.SubMap
      "Code" -> λ(GLOBAL.WeakMap.prototype.get)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.WeakSet.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.WeakSet.prototype
      "name" -> #DESC:GLOBAL.WeakSet.name
      "length" -> #DESC:GLOBAL.WeakSet.length
    }
    #DESC:GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator]
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.entries.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "entries"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AsyncGeneratorResumeNextReturnProcessorRejectedFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions.SubMap
      "Code" -> λ(GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.raw.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "raw"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.asUintN.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.match.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Number.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Map.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Map.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Object.freeze -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.freeze
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.find -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.find
      "Configurable" -> true
    }
    #DESC:GLOBAL.ReferenceError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.toLowerCase -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toLowerCase"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.toLowerCase.SubMap
      "Code" -> λ(GLOBAL.String.prototype.toLowerCase)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.replace -> (Symbol "Symbol.replace")
    #GLOBAL.Array.prototype.indexOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.indexOf.name
      "length" -> #DESC:GLOBAL.Array.prototype.indexOf.length
    }
    #31 -> []
    #DESC:GLOBAL.RangeError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "RangeError"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.unshift.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.unshift.name
      "length" -> #DESC:GLOBAL.Array.prototype.unshift.length
    }
    #GLOBAL.SetIteratorPrototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.SetIteratorPrototype.next.name
      "length" -> #DESC:GLOBAL.SetIteratorPrototype.next.length
    }
    #DESC:GLOBAL.Map.prototype.get.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.reverse -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.reverse
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Symbol.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.keys -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.keys
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.for -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Symbol.for
      "Configurable" -> true
    }
    #GLOBAL.Object.entries -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "entries"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.entries.SubMap
      "Code" -> λ(GLOBAL.Object.entries)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.shift.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.shift.name
      "length" -> #DESC:GLOBAL.Array.prototype.shift.length
    }
    #DESC:GLOBAL.Number.isInteger.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isInteger"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.unshift -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.unshift
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Map"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map[SYMBOL_species].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get [Symbol.species]"
      "Configurable" -> true
    }
    #GLOBAL.Date -> (NotSupported "OrdinaryObject" "GLOBAL.Date")
    #DESC:GLOBAL.Number.MAX_VALUE -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.7976931348623157E308
      "Configurable" -> false
    }
    #DESC:GLOBAL.Promise.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Promise"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.values.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Symbol"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.indexOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.indexOf
      "Configurable" -> true
    }
    #GLOBAL.URIError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.URIError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.CatchFinallyFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "CatchFinallyFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.CatchFinallyFunctions.SubMap
      "Code" -> λ(GLOBAL.CatchFinallyFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakMap.prototype.delete.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "delete"
      "Configurable" -> true
    }
    #GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.asyncIterator]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator].SubMap
      "Code" -> λ(GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map.prototype.forEach -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "forEach"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.forEach.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.forEach)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.flat -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "flat"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.flat.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.flat)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.BigInt.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.BigInt.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Symbol.prototype.description -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Symbol.prototype.description
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #GLOBAL.BigInt -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "BigInt"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.BigInt.SubMap
      "Code" -> λ(GLOBAL.BigInt)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.BigInt64Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt64Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set[SYMBOL_species].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.replaceAll.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.map.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.map.name
      "length" -> #DESC:GLOBAL.Array.prototype.map.length
    }
    #GLOBAL.AsyncGeneratorFunction.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.AsyncGeneratorFunction.prototype[SYMBOL_toStringTag]
      "prototype" -> #DESC:GLOBAL.AsyncGeneratorFunction.prototype.prototype
      "constructor" -> #DESC:GLOBAL.AsyncGeneratorFunction.prototype.constructor
    }
    #GLOBAL.AsyncGeneratorFunction.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.AsyncGeneratorFunction.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.endsWith.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.SubMap -> (TYPE = SubMap) {
      "replaceAll" -> #DESC:GLOBAL.String.prototype.replaceAll
      "toString" -> #DESC:GLOBAL.String.prototype.toString
      "codePointAt" -> #DESC:GLOBAL.String.prototype.codePointAt
      "slice" -> #DESC:GLOBAL.String.prototype.slice
      "startsWith" -> #DESC:GLOBAL.String.prototype.startsWith
      "charAt" -> #DESC:GLOBAL.String.prototype.charAt
      "toUpperCase" -> #DESC:GLOBAL.String.prototype.toUpperCase
      "padStart" -> #DESC:GLOBAL.String.prototype.padStart
      "match" -> #DESC:GLOBAL.String.prototype.match
      "replace" -> #DESC:GLOBAL.String.prototype.replace
      "trim" -> #DESC:GLOBAL.String.prototype.trim
      "trimStart" -> #DESC:GLOBAL.String.prototype.trimStart
      "repeat" -> #DESC:GLOBAL.String.prototype.repeat
      "toLocaleUpperCase" -> #DESC:GLOBAL.String.prototype.toLocaleUpperCase
      #GLOBAL.Symbol.iterator -> #DESC:GLOBAL.String.prototype[SYMBOL_iterator]
      "substring" -> #DESC:GLOBAL.String.prototype.substring
      "padEnd" -> #DESC:GLOBAL.String.prototype.padEnd
      "includes" -> #DESC:GLOBAL.String.prototype.includes
      "localeCompare" -> #DESC:GLOBAL.String.prototype.localeCompare
      "trimEnd" -> #DESC:GLOBAL.String.prototype.trimEnd
      "lastIndexOf" -> #DESC:GLOBAL.String.prototype.lastIndexOf
      "length" -> #DESC:GLOBAL.String.prototype.length
      "normalize" -> #DESC:GLOBAL.String.prototype.normalize
      "constructor" -> #DESC:GLOBAL.String.prototype.constructor
      "toLowerCase" -> #DESC:GLOBAL.String.prototype.toLowerCase
      "indexOf" -> #DESC:GLOBAL.String.prototype.indexOf
      "concat" -> #DESC:GLOBAL.String.prototype.concat
      "charCodeAt" -> #DESC:GLOBAL.String.prototype.charCodeAt
      "split" -> #DESC:GLOBAL.String.prototype.split
      "endsWith" -> #DESC:GLOBAL.String.prototype.endsWith
      "search" -> #DESC:GLOBAL.String.prototype.search
      "toLocaleLowerCase" -> #DESC:GLOBAL.String.prototype.toLocaleLowerCase
      "valueOf" -> #DESC:GLOBAL.String.prototype.valueOf
      "matchAll" -> #DESC:GLOBAL.String.prototype.matchAll
    }
    #GLOBAL.Set.prototype.entries.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.entries.name
      "length" -> #DESC:GLOBAL.Set.prototype.entries.length
    }
    #GLOBAL.WeakSet.prototype.has -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "has"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakSet.prototype.has.SubMap
      "Code" -> λ(GLOBAL.WeakSet.prototype.has)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.toUpperCase.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.toUpperCase.name
      "length" -> #DESC:GLOBAL.String.prototype.toUpperCase.length
    }
    #GLOBAL.Map.prototype.size.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.size.name
      "length" -> #DESC:GLOBAL.Map.prototype.size.length
    }
    #GLOBAL.AsyncGenerator.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.AsyncGenerator.prototype[SYMBOL_toStringTag]
      "return" -> #DESC:GLOBAL.AsyncGenerator.prototype.return
      "constructor" -> #DESC:GLOBAL.AsyncGenerator.prototype.constructor
      "throw" -> #DESC:GLOBAL.AsyncGenerator.prototype.throw
      "next" -> #DESC:GLOBAL.AsyncGenerator.prototype.next
    }
    #GLOBAL.DataView -> (NotSupported "OrdinaryObject" "GLOBAL.DataView")
    #GLOBAL.InternalizeJSONProperty.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.InternalizeJSONProperty.name
      "length" -> #DESC:GLOBAL.InternalizeJSONProperty.length
    }
    #DESC:GLOBAL.Array.prototype.some.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "some"
      "Configurable" -> true
    }
    #DESC:GLOBAL.parseFloat.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.preventExtensions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "preventExtensions"
      "Configurable" -> true
    }
    #60 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> 3.0
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.prototype.includes.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.replaceAll.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.replaceAll.name
      "length" -> #DESC:GLOBAL.String.prototype.replaceAll.length
    }
    #GLOBAL.Set.prototype.entries -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "entries"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.entries.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.entries)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #JOB_QUEUE -> []
    #GLOBAL.Int8Array -> (NotSupported "OrdinaryObject" "GLOBAL.Int8Array")
    #DESC:GLOBAL.$262 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.$262
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.toString.name
      "length" -> #DESC:GLOBAL.String.prototype.toString.length
    }
    #GLOBAL.Array.prototype.flatMap -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "flatMap"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.flatMap.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.flatMap)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.ForInIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.IteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Set" -> λ(OrdinaryObject.Set)
      "SubMap" -> #GLOBAL.ForInIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.return.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.slice.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.slice.name
      "length" -> #DESC:GLOBAL.String.prototype.slice.length
    }
    #GLOBAL.Promise.race.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.race.name
      "length" -> #DESC:GLOBAL.Promise.race.length
    }
    #DESC:GLOBAL.FinalizationRegistry.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "FinalizationRegistry"
      "Configurable" -> true
    }
    #DESC:GLOBAL.URIError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.URIError
      "Configurable" -> true
    }
    #GLOBAL.CatchFinallyFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.CatchFinallyFunctions.name
      "length" -> #DESC:GLOBAL.CatchFinallyFunctions.length
    }
    #GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator].name
      "length" -> #DESC:GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator].length
    }
    #GLOBAL.Map.prototype.size -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get size"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.size.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.size)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.values.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.values.name
      "length" -> #DESC:GLOBAL.Array.prototype.values.length
    }
    #GLOBAL.RangeError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.RangeError.prototype
      "name" -> #DESC:GLOBAL.RangeError.name
      "length" -> #DESC:GLOBAL.RangeError.length
    }
    #DESC:GLOBAL.Symbol.toPrimitive -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.toPrimitive
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.fromCodePoint -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.fromCodePoint
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.size -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get size"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.size.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.size)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise.all.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.all.name
      "length" -> #DESC:GLOBAL.Promise.all.length
    }
    #DESC:GLOBAL.AggregateError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AggregateError.prototype
      "Configurable" -> false
    }
    #GLOBAL.Array.prototype.indexOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "indexOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.indexOf.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.indexOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.isNaN -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isNaN"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.isNaN.SubMap
      "Code" -> λ(GLOBAL.isNaN)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.prototype.hasOwnProperty -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.prototype.hasOwnProperty
      "Configurable" -> true
    }
    #DESC:GLOBAL.Generator.prototype.return.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.toLocaleString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.prototype.toLocaleString.name
      "length" -> #DESC:GLOBAL.Number.prototype.toLocaleString.length
    }
    #DESC:GLOBAL.Symbol.species -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.species
      "Configurable" -> false
    }
    #DESC:GLOBAL.EvalError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> ""
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.prototype.SubMap
      "Code" -> λ(GLOBAL.Function.prototype)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakMap.prototype.delete -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakMap.prototype.delete
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.delete -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "delete"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.delete.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.delete)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.GeneratorFunction.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.GeneratorFunction.prototype
      "name" -> #DESC:GLOBAL.GeneratorFunction.name
      "length" -> #DESC:GLOBAL.GeneratorFunction.length
    }
    #GLOBAL.Object.is -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "is"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.is.SubMap
      "Code" -> λ(GLOBAL.Object.is)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise[SYMBOL_species].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise[SYMBOL_species].name
      "length" -> #DESC:GLOBAL.Promise[SYMBOL_species].length
    }
    #21 -> (TYPE = PendingJob) {
      "ScriptOrModule" -> null
      "Job" -> λ(ScriptEvaluationJob)
      "HostDefined" -> undefined
      "Realm" -> N(#REALM)
      "Arguments" -> #20
    }
    #DESC:GLOBAL.Array.prototype.toLocaleString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.toLocaleString
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncGenerator"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.delete -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.delete
      "Configurable" -> true
    }
    #GLOBAL.Object.getOwnPropertyDescriptors -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "getOwnPropertyDescriptors"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.getOwnPropertyDescriptors.SubMap
      "Code" -> λ(GLOBAL.Object.getOwnPropertyDescriptors)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Set.prototype.has -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "has"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.has.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.has)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].includes -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Object"
      "Configurable" -> true
    }
    #GLOBAL.StringIteratorPrototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.StringIteratorPrototype.next.SubMap
      "Code" -> λ(GLOBAL.StringIteratorPrototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.toLowerCase.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.toLowerCase.name
      "length" -> #DESC:GLOBAL.String.prototype.toLowerCase.length
    }
    #GLOBAL.Symbol.prototype[SYMBOL_toPrimitive] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.toPrimitive]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.prototype[SYMBOL_toPrimitive].SubMap
      "Code" -> λ(GLOBAL.Symbol.prototype[SYMBOL_toPrimitive])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.SyntaxError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "WeakMap"
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.size.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.size.name
      "length" -> #DESC:GLOBAL.Set.prototype.size.length
    }
    #DESC:GLOBAL.Function.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.localeCompare.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.TypedArray.SubMap -> (TYPE = SubMap) {
      "length" -> #DESC:GLOBAL.TypedArray.length
      #GLOBAL.Symbol.species -> #DESC:GLOBAL.TypedArray[SYMBOL_species]
      "name" -> #DESC:GLOBAL.TypedArray.name
      "of" -> #DESC:GLOBAL.TypedArray.of
      "from" -> #DESC:GLOBAL.TypedArray.from
    }
    #GLOBAL.AsyncIteratorPrototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.asyncIterator -> #DESC:GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator]
    }
    #GLOBAL.Object.fromEntries -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "fromEntries"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.fromEntries.SubMap
      "Code" -> λ(GLOBAL.Object.fromEntries)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Set.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.TypeError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.TypeError.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.prototype.matchAll.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "matchAll"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Infinity -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> Infinity
      "Configurable" -> false
    }
    #DESC:GLOBAL.TypeError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.TypeError
      "Configurable" -> true
    }
    #GLOBAL.__ABS__ -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "__ABS__"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.__ABS__.SubMap
      "Code" -> λ(GLOBAL.__ABS__)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Map.prototype.values.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "values"
      "Configurable" -> true
    }
    #5 -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.ThrowTypeError
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> #GLOBAL.ThrowTypeError
    }
    #DESC:GLOBAL.WeakMap.prototype.has.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "has"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.reduce.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.reduce.name
      "length" -> #DESC:GLOBAL.Array.prototype.reduce.length
    }
    #DESC:GLOBAL.Boolean.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.PromiseRejectFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "PromiseRejectFunctions"
      "Configurable" -> true
    }
    #GLOBAL.Symbol.iterator -> (Symbol "Symbol.iterator")
    #GLOBAL.String.fromCharCode.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.fromCharCode.name
      "length" -> #DESC:GLOBAL.String.fromCharCode.length
    }
    #DESC:GLOBAL.Map.prototype.keys -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.keys
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.flat.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.forEach -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "forEach"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.forEach.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.forEach)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Number.isInteger.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.isInteger.name
      "length" -> #DESC:GLOBAL.Number.isInteger.length
    }
    #DESC:GLOBAL.Set.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set
      "Configurable" -> true
    }
    #DESC:GLOBAL.FinalizationRegistry.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.preventExtensions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.preventExtensions
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.toFixed.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.prototype.toFixed.name
      "length" -> #DESC:GLOBAL.Number.prototype.toFixed.length
    }
    #DESC:GLOBAL.encodeURIComponent -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.encodeURIComponent
      "Configurable" -> true
    }
    #GLOBAL.TypedArray[SYMBOL_species].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.TypedArray[SYMBOL_species].name
      "length" -> #DESC:GLOBAL.TypedArray[SYMBOL_species].length
    }
    #GLOBAL.Number.prototype.valueOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.prototype.valueOf.name
      "length" -> #DESC:GLOBAL.Number.prototype.valueOf.length
    }
    #DESC:GLOBAL.Set -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.entries.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.entries.name
      "length" -> #DESC:GLOBAL.Map.prototype.entries.length
    }
    #GLOBAL.Object.isSealed -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isSealed"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.isSealed.SubMap
      "Code" -> λ(GLOBAL.Object.isSealed)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.InternalizeJSONProperty.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 3.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Generator.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Generator"
      "Configurable" -> true
    }
    #DESC:GLOBAL.PromiseRejectFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> ""
      "Configurable" -> true
    }
    #DESC:GLOBAL.GeneratorFunction.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "GeneratorFunction"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.any -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.any
      "Configurable" -> true
    }
    #GLOBAL.String.raw.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.raw.name
      "length" -> #DESC:GLOBAL.String.raw.length
    }
    #GLOBAL.MapIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.IteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.MapIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.EvalError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.startsWith.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.startsWith.name
      "length" -> #DESC:GLOBAL.String.prototype.startsWith.length
    }
    #DESC:GLOBAL.Object.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object
      "Configurable" -> true
    }
    #12 -> (TYPE = SubMap) {}
    #DESC:GLOBAL.Array.prototype.reverse.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.AsyncFromSyncIteratorPrototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncFromSyncIteratorPrototype.next.SubMap
      "Code" -> λ(GLOBAL.AsyncFromSyncIteratorPrototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.AsyncFunction.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.toLocaleUpperCase.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.toLocaleUpperCase.name
      "length" -> #DESC:GLOBAL.String.prototype.toLocaleUpperCase.length
    }
    #DESC:GLOBAL.Object.getOwnPropertyDescriptor.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "getOwnPropertyDescriptor"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ArgGetter.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "ArgGetter"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.values -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "values"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.values.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.values)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncfromSyncIteratorValueUnwrapFunctions"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncGenerator.prototype.next.SubMap
      "Code" -> λ(GLOBAL.AsyncGenerator.prototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.localeCompare.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.localeCompare.name
      "length" -> #DESC:GLOBAL.String.prototype.localeCompare.length
    }
    #GLOBAL.Function.prototype.call -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "call"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.prototype.call.SubMap
      "Code" -> λ(GLOBAL.Function.prototype.call)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ReferenceError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "ReferenceError"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.toLocaleString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toLocaleString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.toLocaleString.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.toLocaleString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.prototype.has.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Set.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.species -> #DESC:GLOBAL.Set[SYMBOL_species]
      "prototype" -> #DESC:GLOBAL.Set.prototype
      "name" -> #DESC:GLOBAL.Set.name
      "length" -> #DESC:GLOBAL.Set.length
    }
    #54 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.print
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toFixed -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.prototype.toFixed
      "Configurable" -> true
    }
    #GLOBAL.RegExp -> (NotSupported "OrdinaryObject" "GLOBAL.RegExp")
    #GLOBAL.AsyncFromSyncIteratorPrototype.return -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "return"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncFromSyncIteratorPrototype.return.SubMap
      "Code" -> λ(GLOBAL.AsyncFromSyncIteratorPrototype.return)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.SubMap -> (TYPE = SubMap) {
      "isExtensible" -> #DESC:GLOBAL.Object.isExtensible
      "setPrototypeOf" -> #DESC:GLOBAL.Object.setPrototypeOf
      "values" -> #DESC:GLOBAL.Object.values
      "seal" -> #DESC:GLOBAL.Object.seal
      "getOwnPropertyDescriptor" -> #DESC:GLOBAL.Object.getOwnPropertyDescriptor
      "keys" -> #DESC:GLOBAL.Object.keys
      "getPrototypeOf" -> #DESC:GLOBAL.Object.getPrototypeOf
      "freeze" -> #DESC:GLOBAL.Object.freeze
      "fromEntries" -> #DESC:GLOBAL.Object.fromEntries
      "create" -> #DESC:GLOBAL.Object.create
      "defineProperty" -> #DESC:GLOBAL.Object.defineProperty
      "assign" -> #DESC:GLOBAL.Object.assign
      "prototype" -> #DESC:GLOBAL.Object.prototype
      "length" -> #DESC:GLOBAL.Object.length
      "defineProperties" -> #DESC:GLOBAL.Object.defineProperties
      "isFrozen" -> #DESC:GLOBAL.Object.isFrozen
      "isSealed" -> #DESC:GLOBAL.Object.isSealed
      "getOwnPropertyDescriptors" -> #DESC:GLOBAL.Object.getOwnPropertyDescriptors
      "getOwnPropertyNames" -> #DESC:GLOBAL.Object.getOwnPropertyNames
      "entries" -> #DESC:GLOBAL.Object.entries
      "is" -> #DESC:GLOBAL.Object.is
      "getOwnPropertySymbols" -> #DESC:GLOBAL.Object.getOwnPropertySymbols
      "name" -> #DESC:GLOBAL.Object.name
      "preventExtensions" -> #DESC:GLOBAL.Object.preventExtensions
    }
    #DESC:GLOBAL.parseInt.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.find.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.BigInt.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.BigInt.prototype
      "asIntN" -> #DESC:GLOBAL.BigInt.asIntN
      "length" -> #DESC:GLOBAL.BigInt.length
      "name" -> #DESC:GLOBAL.BigInt.name
      "asUintN" -> #DESC:GLOBAL.BigInt.asUintN
    }
    #DESC:GLOBAL.Array.prototype.every -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.every
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.seal.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorFunction.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AsyncGeneratorFunction
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.toLocaleString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.toLocaleString.name
      "length" -> #DESC:GLOBAL.Array.prototype.toLocaleString.length
    }
    #DESC:GLOBAL.Promise.prototype.catch -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.prototype.catch
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.isPrototypeOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isPrototypeOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.find.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "find"
      "Configurable" -> true
    }
    #GLOBAL.Object.getPrototypeOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.getPrototypeOf.name
      "length" -> #DESC:GLOBAL.Object.getPrototypeOf.length
    }
    #GLOBAL.RangeError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.RangeError.prototype.name
      "constructor" -> #DESC:GLOBAL.RangeError.prototype.constructor
      "message" -> #DESC:GLOBAL.RangeError.prototype.message
    }
    #GLOBAL.GeneratorFunction.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.GeneratorFunction.prototype[SYMBOL_toStringTag]
      "prototype" -> #DESC:GLOBAL.GeneratorFunction.prototype.prototype
      "constructor" -> #DESC:GLOBAL.GeneratorFunction.prototype.constructor
    }
    #DESC:GLOBAL.Promise.race.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "race"
      "Configurable" -> true
    }
    #GLOBAL.Promise.any.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.any.name
      "length" -> #DESC:GLOBAL.Promise.any.length
    }
    #GLOBAL.Array.prototype.forEach -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "forEach"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.forEach.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.forEach)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.prototype.finally.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.is.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.is.name
      "length" -> #DESC:GLOBAL.Object.is.length
    }
    #GLOBAL.Object.prototype.propertyIsEnumerable -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "propertyIsEnumerable"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.prototype.propertyIsEnumerable.SubMap
      "Code" -> λ(GLOBAL.Object.prototype.propertyIsEnumerable)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Promise.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.WeakSet.prototype.delete.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakSet.prototype.delete.name
      "length" -> #DESC:GLOBAL.WeakSet.prototype.delete.length
    }
    #GLOBAL.Array.prototype.reduceRight -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "reduceRight"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.reduceRight.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.reduceRight)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.join.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.parseInt -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.parseInt
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.slice -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "slice"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.slice.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.slice)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.TypeError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.AsyncFromSyncIteratorPrototype.SubMap -> (TYPE = SubMap) {
      "throw" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.throw
      "next" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.next
      "return" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.return
    }
    #DESC:GLOBAL.WeakSet.prototype.add -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakSet.prototype.add
      "Configurable" -> true
    }
    #DESC:GLOBAL.AwaitRejectedFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AwaitRejectedFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.fill.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.lastIndexOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "lastIndexOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ForInIteratorPrototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ForInIteratorPrototype.next
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.get.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.get.name
      "length" -> #DESC:GLOBAL.Map.prototype.get.length
    }
    #DESC:GLOBAL.String.prototype.charAt.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "charAt"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.matchAll -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "matchAll"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.matchAll.SubMap
      "Code" -> λ(GLOBAL.String.prototype.matchAll)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.isConcatSpreadable -> (Symbol "Symbol.isConcatSpreadable")
    #DESC:GLOBAL.RangeError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.RangeError
      "Configurable" -> true
    }
    #GLOBAL.Promise.prototype.finally.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.prototype.finally.name
      "length" -> #DESC:GLOBAL.Promise.prototype.finally.length
    }
    #DESC:GLOBAL.Number.isNaN.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.split.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #49 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #DESC:GLOBAL.Number.isFinite.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isFinite"
      "Configurable" -> true
    }
    #40 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #GLOBAL.AsyncFromSyncIteratorPrototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.next.name
      "length" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.next.length
    }
    #GLOBAL.Int32Array -> (NotSupported "OrdinaryObject" "GLOBAL.Int32Array")
    #GLOBAL.SharedArrayBuffer -> (NotSupported "OrdinaryObject" "GLOBAL.SharedArrayBuffer")
    #DESC:GLOBAL.ArrayIteratorPrototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.codePointAt.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "codePointAt"
      "Configurable" -> true
    }
    #GLOBAL.PromiseResolveFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.PromiseResolveFunctions.name
      "length" -> #DESC:GLOBAL.PromiseResolveFunctions.length
    }
    #DESC:GLOBAL.IfAbruptRejectPromise.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "IfAbruptRejectPromise"
      "Configurable" -> true
    }
    #DESC:GLOBAL.InternalizeJSONProperty.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "InternalizeJSONProperty"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.fromEntries.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.set -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.set
      "Configurable" -> true
    }
    #GLOBAL.ArgGetter.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ArgGetter.name
      "length" -> #DESC:GLOBAL.ArgGetter.length
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.throw.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "throw"
      "Configurable" -> true
    }
    #GLOBAL.print -> (TYPE = BuiltinFunctionObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.print.SubMap
      "Code" -> λ(GLOBAL.HostPrint)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Set.prototype.clear -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "clear"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.clear.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.clear)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.repeat.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype[SYMBOL_iterator] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.iterator]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype[SYMBOL_iterator].SubMap
      "Code" -> λ(GLOBAL.String.prototype[SYMBOL_iterator])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.pop.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "pop"
      "Configurable" -> true
    }
    #DESC:GLOBAL.encodeURIComponent.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "encodeURIComponent"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map[SYMBOL_species].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigUint64Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigUint64Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.POSITIVE_INFINITY -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> Infinity
      "Configurable" -> false
    }
    #GLOBAL.Atomics -> (NotSupported "OrdinaryObject" "GLOBAL.Atomics")
    #7 -> []
    #DESC:GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.includes.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "includes"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.setPrototypeOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "setPrototypeOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Math -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Math
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Map.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.flat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.flat
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.unscopables -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.unscopables
      "Configurable" -> false
    }
    #24 -> (TYPE = ScriptRecord) {
      "Environment" -> undefined
      "ECMAScriptCode" -> ☊[ScriptBody](var x = 1 + 2 ; print ( x ) ;)
      "Realm" -> #REALM
      "HostDefined" -> undefined
    }
    #GLOBAL.IfAbruptRejectPromise -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "IfAbruptRejectPromise"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.IfAbruptRejectPromise.SubMap
      "Code" -> λ(GLOBAL.IfAbruptRejectPromise)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Number.isSafeInteger -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.isSafeInteger
      "Configurable" -> true
    }
    #GLOBAL.SetIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.IteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.SetIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.lastIndexOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "lastIndexOf"
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Symbol.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.replace.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.isNaN -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.isNaN
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.toLocaleString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toLocaleString"
      "Configurable" -> true
    }
    #GLOBAL.Generator.prototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Generator.prototype.next.name
      "length" -> #DESC:GLOBAL.Generator.prototype.next.length
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Object.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Map.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Map"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.keys.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "keys"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.AggregateError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #SYMBOL_REGISTRY -> []
    #DESC:GLOBAL.Promise.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Promise"
      "Configurable" -> true
    }
    #GLOBAL.Number.isSafeInteger.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.isSafeInteger.name
      "length" -> #DESC:GLOBAL.Number.isSafeInteger.length
    }
    #59 -> (TYPE = ReferenceRecord) {
      "ThisValue" -> ~empty~
      "Base" -> N(#17)
      "Strict" -> true
      "ReferencedName" -> N("x")
    }
    #GLOBAL.Array.prototype.some.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.some.name
      "length" -> #DESC:GLOBAL.Array.prototype.some.length
    }
    #GLOBAL.Number.prototype.toLocaleString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toLocaleString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.prototype.toLocaleString.SubMap
      "Code" -> λ(GLOBAL.Number.prototype.toLocaleString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.defineProperty.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "defineProperty"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncFunction.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncFunction"
      "Configurable" -> true
    }
    #GLOBAL.Array[SYMBOL_species] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get [Symbol.species]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array[SYMBOL_species].SubMap
      "Code" -> λ(GLOBAL.Array[SYMBOL_species])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.values -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "values"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.values.SubMap
      "Code" -> λ(GLOBAL.Object.values)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise.race -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "race"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.race.SubMap
      "Code" -> λ(GLOBAL.Promise.race)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Symbol.prototype.valueOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "valueOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.set -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakMap.prototype.set
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.return -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncGenerator.prototype.return
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getOwnPropertyDescriptor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.getOwnPropertyDescriptor
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.values -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.values
      "Configurable" -> true
    }
    #DESC:GLOBAL.AwaitRejectedFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.trimEnd -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "trimEnd"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.trimEnd.SubMap
      "Code" -> λ(GLOBAL.String.prototype.trimEnd)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.prototype.toLocaleString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toLocaleString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Function.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Map.prototype.clear.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "clear"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.startsWith -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.startsWith
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.normalize.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.normalize.name
      "length" -> #DESC:GLOBAL.String.prototype.normalize.length
    }
    #DESC:GLOBAL.Number.MIN_VALUE -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 4.9E-324
      "Configurable" -> false
    }
    #DESC:GLOBAL.SetIteratorPrototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.SetIteratorPrototype.next
      "Configurable" -> true
    }
    #DESC:GLOBAL.isNaN.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isNaN"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.size.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get size"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.create.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.map.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Uint32Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Uint32Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncIteratorPrototype[SYMBOL_asyncIterator].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.asyncIterator]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AggregateError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AggregateError"
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype.apply.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Function.prototype.apply.name
      "length" -> #DESC:GLOBAL.Function.prototype.apply.length
    }
    #DESC:GLOBAL.Array.prototype.slice -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.slice
      "Configurable" -> true
    }
    #GLOBAL.TypeError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "TypeError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.TypeError.SubMap
      "Code" -> λ(GLOBAL.TypeError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.startsWith.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map
      "Configurable" -> true
    }
    #DESC:GLOBAL.SyntaxError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "SyntaxError"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.includes.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.includes.name
      "length" -> #DESC:GLOBAL.Array.prototype.includes.length
    }
    #DESC:GLOBAL.ProxyRevocationFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.copyWithin.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "copyWithin"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.substring.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "substring"
      "Configurable" -> true
    }
    #GLOBAL.Boolean.prototype.SubMap -> (TYPE = SubMap) {
      "toString" -> #DESC:GLOBAL.Boolean.prototype.toString
      "valueOf" -> #DESC:GLOBAL.Boolean.prototype.valueOf
      "constructor" -> #DESC:GLOBAL.Boolean.prototype.constructor
    }
    #DESC:GLOBAL.Map.prototype.keys.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.call.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #13 -> (TYPE = ObjectEnvironmentRecord) {
      "InitializeBinding" -> λ(ObjectEnvironmentRecord.InitializeBinding)
      "WithBaseObject" -> λ(ObjectEnvironmentRecord.WithBaseObject)
      "DeleteBinding" -> λ(ObjectEnvironmentRecord.DeleteBinding)
      "CreateMutableBinding" -> λ(ObjectEnvironmentRecord.CreateMutableBinding)
      "withEnvironment" -> false
      "BindingObject" -> #11
      "GetBindingValue" -> λ(ObjectEnvironmentRecord.GetBindingValue)
      "HasBinding" -> λ(ObjectEnvironmentRecord.HasBinding)
      "SubMap" -> #12
      "HasSuperBinding" -> λ(ObjectEnvironmentRecord.HasSuperBinding)
      "HasThisBinding" -> λ(ObjectEnvironmentRecord.HasThisBinding)
      "SetMutableBinding" -> λ(ObjectEnvironmentRecord.SetMutableBinding)
    }
    #14 -> (TYPE = SubMap) {}
    #GLOBAL.ArrayIteratorPrototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ArrayIteratorPrototype.next.SubMap
      "Code" -> λ(GLOBAL.ArrayIteratorPrototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.every.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.every.name
      "length" -> #DESC:GLOBAL.Array.prototype.every.length
    }
    #GLOBAL.Object.prototype.toLocaleString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.prototype.toLocaleString.name
      "length" -> #DESC:GLOBAL.Object.prototype.toLocaleString.length
    }
    #GLOBAL.TypedArray.from -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "from"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.TypedArray.from.SubMap
      "Code" -> λ(GLOBAL.TypedArray.from)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Generator.prototype.return.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Generator.prototype.return.name
      "length" -> #DESC:GLOBAL.Generator.prototype.return.length
    }
    #DESC:GLOBAL.Function.prototype.bind.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.GetCapabilitiesExecutorFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.GetCapabilitiesExecutorFunctions
      "Configurable" -> true
    }
    #GLOBAL.InternalizeJSONProperty -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "InternalizeJSONProperty"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.InternalizeJSONProperty.SubMap
      "Code" -> λ(GLOBAL.InternalizeJSONProperty)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.AsyncFunction -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncFunction.SubMap
      "Code" -> λ(GLOBAL.AsyncFunction)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.URIError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.URIError.prototype
      "name" -> #DESC:GLOBAL.URIError.name
      "length" -> #DESC:GLOBAL.URIError.length
    }
    #DESC:GLOBAL.Error.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.raw.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.HostPrint.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.HostPrint.name
      "length" -> #DESC:GLOBAL.HostPrint.length
    }
    #GLOBAL.Number.isNaN -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isNaN"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.isNaN.SubMap
      "Code" -> λ(GLOBAL.Number.isNaN)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.matchAll -> (Symbol "Symbol.matchAll")
    #GLOBAL.String.prototype.padEnd.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.padEnd.name
      "length" -> #DESC:GLOBAL.String.prototype.padEnd.length
    }
    #DESC:GLOBAL.String.prototype.substring.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "WeakSet"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.endsWith.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "endsWith"
      "Configurable" -> true
    }
    #GLOBAL.Set[SYMBOL_species] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get [Symbol.species]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set[SYMBOL_species].SubMap
      "Code" -> λ(GLOBAL.Set[SYMBOL_species])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array[SYMBOL_species].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array[SYMBOL_species].name
      "length" -> #DESC:GLOBAL.Array[SYMBOL_species].length
    }
    #DESC:GLOBAL.Array.prototype.splice.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype[SYMBOL_iterator] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype[SYMBOL_iterator]
      "Configurable" -> true
    }
    #GLOBAL.parseFloat -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "parseFloat"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.parseFloat.SubMap
      "Code" -> λ(GLOBAL.parseFloat)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Symbol.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Symbol"
      "Configurable" -> true
    }
    #DESC:GLOBAL.HostPrint -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.HostPrint
      "Configurable" -> true
    }
    #33 -> []
    #DESC:GLOBAL.Function.prototype.call.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "call"
      "Configurable" -> true
    }
    #DESC:GLOBAL.PromiseResolveFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "PromiseResolveFunctions"
      "Configurable" -> true
    }
    #GLOBAL.Object.seal.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.seal.name
      "length" -> #DESC:GLOBAL.Object.seal.length
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.throw -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncFromSyncIteratorPrototype.throw
      "Configurable" -> true
    }
    #GLOBAL.RangeError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.RangeError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Generator.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.IteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Generator.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.values.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "values"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.repeat.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.repeat.name
      "length" -> #DESC:GLOBAL.String.prototype.repeat.length
    }
    #GLOBAL.Uint32Array -> (NotSupported "OrdinaryObject" "GLOBAL.Uint32Array")
    #GLOBAL.Map.prototype.values -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "values"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.values.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.values)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.all.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.freeze.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.freeze.name
      "length" -> #DESC:GLOBAL.Object.freeze.length
    }
    #DESC:GLOBAL.Array.of -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.of
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.valueOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "valueOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.prototype.valueOf.SubMap
      "Code" -> λ(GLOBAL.Object.prototype.valueOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.BigInt.asUintN -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt.asUintN
      "Configurable" -> true
    }
    #19 -> ["print", "$262", "globalThis", "Infinity", "NaN", "undefined", "Array", "ArrayBuffer", "BigInt64Array", "BigUint64Array", "Boolean", "DataView", "Date", "Error", "EvalError", "Float32Array", "Float64Array", "Function", "Int8Array", "Int16Array", "Int32Array", "Map", "Number", "BigInt", "Object", "Promise", "Proxy", "RangeError", "ReferenceError", "RegExp", "Set", "SharedArrayBuffer", "String", "Symbol", "SyntaxError", "TypeError", "Uint8Array", "Uint8ClampedArray", "Uint16Array", "Uint32Array", "URIError", "WeakMap", "WeakSet", "Atomics", "JSON", "Math", "Reflect", "HostPrint", "isNaN", "AwaitFulfilledFunctions", "TypedArray", "AsyncGeneratorFunction", "decodeURIComponent", "PromiseRejectFunctions", "encodeURIComponent", "PromiseResolveFunctions", "ThrowTypeError", "GetCapabilitiesExecutorFunctions", "parseFloat", "ArgGetter", "ThenFinallyFunctions", "AsyncGeneratorResumeNextReturnProcessorRejectedFunctions", "GeneratorFunction", "InternalizeJSONProperty", "parseInt", "decodeURI", "AggregateError", "CatchFinallyFunctions", "__ABS__", "isFinite", "FinalizationRegistry", "ProxyRevocationFunctions", "DefaultConstructorFunctions", "encodeURI", "AwaitRejectedFunctions", "CreateDataPropertyOnObjectFunctions", "ArgSetter", "eval", "AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions", "AsyncfromSyncIteratorValueUnwrapFunctions", "IfAbruptRejectPromise"]
    #DESC:GLOBAL.ProxyRevocationFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "ProxyRevocationFunctions"
      "Configurable" -> true
    }
    #GLOBAL.Symbol.for.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Symbol.for.name
      "length" -> #DESC:GLOBAL.Symbol.for.length
    }
    #GLOBAL.Object.preventExtensions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.preventExtensions.name
      "length" -> #DESC:GLOBAL.Object.preventExtensions.length
    }
    #GLOBAL.WeakMap.prototype.get.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakMap.prototype.get.name
      "length" -> #DESC:GLOBAL.WeakMap.prototype.get.length
    }
    #GLOBAL.Array.prototype.filter.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.filter.name
      "length" -> #DESC:GLOBAL.Array.prototype.filter.length
    }
    #DESC:GLOBAL.Array.prototype.concat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.concat
      "Configurable" -> true
    }
    #GLOBAL.Object.seal -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "seal"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.seal.SubMap
      "Code" -> λ(GLOBAL.Object.seal)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Symbol.match -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.match
      "Configurable" -> false
    }
    #GLOBAL.BigInt.asUintN -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "asUintN"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.BigInt.asUintN.SubMap
      "Code" -> λ(GLOBAL.BigInt.asUintN)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #61 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> 3.0
      "Configurable" -> false
    }
    #DESC:GLOBAL.Function.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getOwnPropertySymbols.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.sort -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "sort"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.sort.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.sort)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.isArray.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.isArray.name
      "length" -> #DESC:GLOBAL.Array.isArray.length
    }
    #DESC:GLOBAL.TypeError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "TypeError"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #42 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #GLOBAL.TypedArray.of.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.TypedArray.of.name
      "length" -> #DESC:GLOBAL.TypedArray.of.length
    }
    #GLOBAL.AggregateError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.AggregateError.prototype
      "name" -> #DESC:GLOBAL.AggregateError.name
      "length" -> #DESC:GLOBAL.AggregateError.length
    }
    #GLOBAL.encodeURI -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "encodeURI"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.encodeURI.SubMap
      "Code" -> λ(GLOBAL.encodeURI)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.defineProperty -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.defineProperty
      "Configurable" -> true
    }
    #29 -> []
    #DESC:GLOBAL.Set.prototype.keys -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.values
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.toLocaleUpperCase -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.toLocaleUpperCase
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.has.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "has"
      "Configurable" -> true
    }
    #DESC:GLOBAL.print -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.print
      "Configurable" -> true
    }
    #GLOBAL.eval -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "eval"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.eval.SubMap
      "Code" -> λ(GLOBAL.eval)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.toLowerCase.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toLowerCase"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].values -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.concat.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Promise.reject.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.reject.name
      "length" -> #DESC:GLOBAL.Promise.reject.length
    }
    #DESC:GLOBAL.Array.prototype.indexOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.indexOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.split -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.split
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.reduce -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "reduce"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.reduce.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.reduce)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Function.prototype.SubMap -> (TYPE = SubMap) {
      "toString" -> #DESC:GLOBAL.Function.prototype.toString
      "call" -> #DESC:GLOBAL.Function.prototype.call
      #GLOBAL.Symbol.hasInstance -> #DESC:GLOBAL.Function.prototype[SYMBOL_hasInstance]
      "arguments" -> #DESC:GLOBAL.Function.prototype.arguments
      "length" -> #DESC:GLOBAL.Function.prototype.length
      "constructor" -> #DESC:GLOBAL.Function.prototype.constructor
      "bind" -> #DESC:GLOBAL.Function.prototype.bind
      "apply" -> #DESC:GLOBAL.Function.prototype.apply
      "caller" -> #DESC:GLOBAL.Function.prototype.caller
      "name" -> #DESC:GLOBAL.Function.prototype.name
    }
    #GLOBAL.AwaitRejectedFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AwaitRejectedFunctions.name
      "length" -> #DESC:GLOBAL.AwaitRejectedFunctions.length
    }
    #DESC:GLOBAL.Array.prototype.push.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.$262 -> (NotSupported "OrdinaryObject" "GLOBAL.$262")
    #DESC:GLOBAL.TypeError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.slice.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "slice"
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.iterator -> #DESC:GLOBAL.Set.prototype[SYMBOL_iterator]
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.Set.prototype[SYMBOL_toStringTag]
      "size" -> #DESC:GLOBAL.Set.prototype.size
      "delete" -> #DESC:GLOBAL.Set.prototype.delete
      "add" -> #DESC:GLOBAL.Set.prototype.add
      "forEach" -> #DESC:GLOBAL.Set.prototype.forEach
      "entries" -> #DESC:GLOBAL.Set.prototype.entries
      "has" -> #DESC:GLOBAL.Set.prototype.has
      "values" -> #DESC:GLOBAL.Set.prototype.values
      "clear" -> #DESC:GLOBAL.Set.prototype.clear
      "constructor" -> #DESC:GLOBAL.Set.prototype.constructor
      "keys" -> #DESC:GLOBAL.Set.prototype.keys
    }
    #DESC:GLOBAL.String.prototype.split.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "split"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Generator.prototype.throw -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Generator.prototype.throw
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.clear.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "clear"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.fromCharCode.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.search -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.search
      "Configurable" -> false
    }
    #DESC:GLOBAL.TypedArray.from -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.TypedArray.from
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorFunction.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.decodeURI.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.AggregateError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AggregateError
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.replace -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.replace
      "Configurable" -> false
    }
    #GLOBAL.Set.prototype.add -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "add"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.add.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.add)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.decodeURI.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.decodeURI.name
      "length" -> #DESC:GLOBAL.decodeURI.length
    }
    #DESC:GLOBAL.globalThis -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #11
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.trim.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.trim.name
      "length" -> #DESC:GLOBAL.String.prototype.trim.length
    }
    #DESC:GLOBAL.Set[SYMBOL_species] -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Set[SYMBOL_species]
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #GLOBAL.WeakMap.prototype.has -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "has"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakMap.prototype.has.SubMap
      "Code" -> λ(GLOBAL.WeakMap.prototype.has)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.is -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.is
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.search.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "search"
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.has.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.has.name
      "length" -> #DESC:GLOBAL.Map.prototype.has.length
    }
    #GLOBAL.String.prototype.toLocaleUpperCase -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toLocaleUpperCase"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.toLocaleUpperCase.SubMap
      "Code" -> λ(GLOBAL.String.prototype.toLocaleUpperCase)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.WeakMap.prototype.delete.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakMap.prototype.delete.name
      "length" -> #DESC:GLOBAL.WeakMap.prototype.delete.length
    }
    #DESC:GLOBAL.Object.prototype.valueOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.prototype.valueOf
      "Configurable" -> true
    }
    #GLOBAL.Function.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.Function.prototype
      "name" -> #DESC:GLOBAL.Function.name
      "length" -> #DESC:GLOBAL.Function.length
    }
    #GLOBAL.Map.prototype.set.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.set.name
      "length" -> #DESC:GLOBAL.Map.prototype.set.length
    }
    #DESC:GLOBAL.SyntaxError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "SyntaxError"
      "Configurable" -> true
    }
    #GLOBAL.Uint8ClampedArray -> (NotSupported "OrdinaryObject" "GLOBAL.Uint8ClampedArray")
    #GLOBAL.Object.setPrototypeOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.setPrototypeOf.name
      "length" -> #DESC:GLOBAL.Object.setPrototypeOf.length
    }
    #38 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #DESC:GLOBAL.Function.prototype.call -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Function.prototype.call
      "Configurable" -> true
    }
    #GLOBAL.SetIteratorPrototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.SetIteratorPrototype[SYMBOL_toStringTag]
      "next" -> #DESC:GLOBAL.SetIteratorPrototype.next
    }
    #DESC:GLOBAL.Symbol.prototype.description.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get description"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.propertyIsEnumerable -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.prototype.propertyIsEnumerable
      "Configurable" -> true
    }
    #DESC:GLOBAL.parseInt.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "parseInt"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype[SYMBOL_iterator] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.entries
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.return.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.__ABS__ -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.__ABS__
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.valueOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "valueOf"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.valueOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.valueOf.name
      "length" -> #DESC:GLOBAL.String.prototype.valueOf.length
    }
    #DESC:GLOBAL.RangeError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype.description.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.WeakMap.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.WeakMap.prototype[SYMBOL_toStringTag]
      "get" -> #DESC:GLOBAL.WeakMap.prototype.get
      "delete" -> #DESC:GLOBAL.WeakMap.prototype.delete
      "set" -> #DESC:GLOBAL.WeakMap.prototype.set
      "constructor" -> #DESC:GLOBAL.WeakMap.prototype.constructor
      "has" -> #DESC:GLOBAL.WeakMap.prototype.has
    }
    #GLOBAL.Number.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Number.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "NumberData" -> 0.0
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getOwnPropertyDescriptors -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.getOwnPropertyDescriptors
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype[SYMBOL_iterator].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.iterator]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.has.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.SubMap -> (TYPE = SubMap) {
      "toString" -> #DESC:GLOBAL.Object.prototype.toString
      "toLocaleString" -> #DESC:GLOBAL.Object.prototype.toLocaleString
      "constructor" -> #DESC:GLOBAL.Object.prototype.constructor
      "propertyIsEnumerable" -> #DESC:GLOBAL.Object.prototype.propertyIsEnumerable
      "isPrototypeOf" -> #DESC:GLOBAL.Object.prototype.isPrototypeOf
      "valueOf" -> #DESC:GLOBAL.Object.prototype.valueOf
      "hasOwnProperty" -> #DESC:GLOBAL.Object.prototype.hasOwnProperty
    }
    #DESC:GLOBAL.Object.fromEntries.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "fromEntries"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.values -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.values
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.reduceRight -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.reduceRight
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Symbol.prototype.toString
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.IfAbruptRejectPromise.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.IfAbruptRejectPromise.name
      "length" -> #DESC:GLOBAL.IfAbruptRejectPromise.length
    }
    #DESC:GLOBAL.Error.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Error.prototype
      "Configurable" -> false
    }
    #GLOBAL.Array.prototype.pop.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.pop.name
      "length" -> #DESC:GLOBAL.Array.prototype.pop.length
    }
    #DESC:GLOBAL.Array.from.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.of.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.entries -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.entries
      "Configurable" -> true
    }
    #GLOBAL.Promise.resolve.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.resolve.name
      "length" -> #DESC:GLOBAL.Promise.resolve.length
    }
    #GLOBAL.Promise -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Promise"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.SubMap
      "Code" -> λ(GLOBAL.Promise)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.trim.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.values -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.values
      "Configurable" -> true
    }
    #39 -> (TYPE = DataProperty) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> 3.0
      "Configurable" -> false
    }
    #DESC:GLOBAL.WeakSet.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.prototype.add.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "add"
      "Configurable" -> true
    }
    #DESC:GLOBAL.StringIteratorPrototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.StringIteratorPrototype.next
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.normalize -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "normalize"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.normalize.SubMap
      "Code" -> λ(GLOBAL.String.prototype.normalize)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.AsyncGeneratorFunction -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AsyncGeneratorFunction"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncGeneratorFunction.SubMap
      "Code" -> λ(GLOBAL.AsyncGeneratorFunction)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.BigInt.asIntN -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "asIntN"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.BigInt.asIntN.SubMap
      "Code" -> λ(GLOBAL.BigInt.asIntN)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.from -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "from"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.from.SubMap
      "Code" -> λ(GLOBAL.Array.from)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.trimStart -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.trimStart
      "Configurable" -> true
    }
    #GLOBAL.ThenFinallyFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ThenFinallyFunctions.name
      "length" -> #DESC:GLOBAL.ThenFinallyFunctions.length
    }
    #DESC:GLOBAL.Error -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Error
      "Configurable" -> true
    }
    #DESC:GLOBAL.StringIteratorPrototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.forEach.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.is.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "is"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.charAt.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.normalize -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.normalize
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.trimEnd.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "trimEnd"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.concat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.concat
      "Configurable" -> true
    }
    #DESC:GLOBAL.ThrowTypeError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ThrowTypeError
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Symbol
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toLocaleString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.prototype.toLocaleString
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype.valueOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "valueOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.prototype.valueOf.SubMap
      "Code" -> λ(GLOBAL.Symbol.prototype.valueOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Number.isNaN -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.isNaN
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.map -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.map
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.values.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.fromCharCode.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "fromCharCode"
      "Configurable" -> true
    }
    #GLOBAL.BigInt.prototype.valueOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "valueOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.BigInt.prototype.valueOf.SubMap
      "Code" -> λ(GLOBAL.BigInt.prototype.valueOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.BigInt64Array -> (NotSupported "OrdinaryObject" "GLOBAL.BigInt64Array")
    #REALM.SubMap -> (TYPE = SubMap) {}
    #DESC:GLOBAL.IteratorPrototype[SYMBOL_iterator].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.iterator]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ThenFinallyFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ThenFinallyFunctions
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.padStart -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "padStart"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.padStart.SubMap
      "Code" -> λ(GLOBAL.String.prototype.padStart)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.URIError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "URIError"
      "Configurable" -> true
    }
    #GLOBAL.Float32Array -> (NotSupported "OrdinaryObject" "GLOBAL.Float32Array")
    #DESC:GLOBAL.Object.freeze.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "freeze"
      "Configurable" -> true
    }
    #51 -> (TYPE = PropertyDescriptor) {
      "Value" -> 3.0
    }
    #GLOBAL.Promise.resolve -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "resolve"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.resolve.SubMap
      "Code" -> λ(GLOBAL.Promise.resolve)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.BigInt.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.BigInt.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.BigInt.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.fill -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "fill"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.fill.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.fill)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.keys.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.toLocaleString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.InternalizeJSONProperty -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.InternalizeJSONProperty
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #GLOBAL.Error.prototype.SubMap -> (TYPE = SubMap) {
      "toString" -> #DESC:GLOBAL.Error.prototype.toString
      "name" -> #DESC:GLOBAL.Error.prototype.name
      "constructor" -> #DESC:GLOBAL.Error.prototype.constructor
      "message" -> #DESC:GLOBAL.Error.prototype.message
    }
    #43 -> (TYPE = PropertyDescriptor) {
      "Value" -> undefined
    }
    #GLOBAL.Function.prototype.apply -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "apply"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.prototype.apply.SubMap
      "Code" -> λ(GLOBAL.Function.prototype.apply)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.prototype.entries.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.WeakSet.prototype
      "Configurable" -> false
    }
    #GLOBAL.String.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.String.prototype
      "length" -> #DESC:GLOBAL.String.length
      "fromCharCode" -> #DESC:GLOBAL.String.fromCharCode
      "fromCodePoint" -> #DESC:GLOBAL.String.fromCodePoint
      "name" -> #DESC:GLOBAL.String.name
      "raw" -> #DESC:GLOBAL.String.raw
    }
    #DESC:GLOBAL.decodeURIComponent.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "decodeURIComponent"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.reduce.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "reduce"
      "Configurable" -> true
    }
    #36 -> []
    #GLOBAL.ProxyRevocationFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "ProxyRevocationFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ProxyRevocationFunctions.SubMap
      "Code" -> λ(GLOBAL.ProxyRevocationFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise.reject -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "reject"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.reject.SubMap
      "Code" -> λ(GLOBAL.Promise.reject)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.toLocaleUpperCase.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Object.entries.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.entries.name
      "length" -> #DESC:GLOBAL.Object.entries.length
    }
    #DESC:GLOBAL.String.fromCharCode -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.fromCharCode
      "Configurable" -> true
    }
    #DESC:GLOBAL.Error.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Error.prototype.toString
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.filter -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "filter"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.filter.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.filter)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Boolean.prototype.valueOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Boolean.prototype.valueOf
      "Configurable" -> true
    }
    #GLOBAL.Reflect -> (NotSupported "OrdinaryObject" "GLOBAL.Reflect")
    #GLOBAL.Set -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Set"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.SubMap
      "Code" -> λ(GLOBAL.Set)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Reflect -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Reflect
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype.valueOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.search -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.search
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.keys -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.keys
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.prototype.valueOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "valueOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.clear -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.clear
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.reduceRight.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.toLocaleString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.keys.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "keys"
      "Configurable" -> true
    }
    #GLOBAL.Object.defineProperties -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "defineProperties"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.defineProperties.SubMap
      "Code" -> λ(GLOBAL.Object.defineProperties)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.assign.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "assign"
      "Configurable" -> true
    }
    #GLOBAL.Object.values.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.values.name
      "length" -> #DESC:GLOBAL.Object.values.length
    }
    #DESC:GLOBAL.Object.freeze.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.localeCompare.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "localeCompare"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.prototype.then -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.prototype.then
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.indexOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "indexOf"
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype.bind.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Function.prototype.bind.name
      "length" -> #DESC:GLOBAL.Function.prototype.bind.length
    }
    #DESC:GLOBAL.Number -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number
      "Configurable" -> true
    }
    #DESC:GLOBAL.DefaultConstructorFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "DefaultConstructorFunctions"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ThenFinallyFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Error.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Object.defineProperty -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "defineProperty"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.defineProperty.SubMap
      "Code" -> λ(GLOBAL.Object.defineProperty)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.lastIndexOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.lastIndexOf.name
      "length" -> #DESC:GLOBAL.Array.prototype.lastIndexOf.length
    }
    #DESC:GLOBAL.Generator.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.GeneratorFunction.prototype
      "Configurable" -> true
    }
    #DESC:GLOBAL.encodeURI.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.EvalError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.EvalError
      "Configurable" -> true
    }
    #DESC:GLOBAL.eval.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype.SubMap -> (TYPE = SubMap) {
      "toString" -> #DESC:GLOBAL.Symbol.prototype.toString
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.Symbol.prototype[SYMBOL_toStringTag]
      "description" -> #DESC:GLOBAL.Symbol.prototype.description
      "constructor" -> #DESC:GLOBAL.Symbol.prototype.constructor
      #GLOBAL.Symbol.toPrimitive -> #DESC:GLOBAL.Symbol.prototype[SYMBOL_toPrimitive]
      "valueOf" -> #DESC:GLOBAL.Symbol.prototype.valueOf
    }
    #GLOBAL.Array.prototype.every -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "every"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.every.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.every)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.splice -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.splice
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.codePointAt.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.WeakMap.prototype
      "Configurable" -> false
    }
    #GLOBAL.ThenFinallyFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "ThenFinallyFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ThenFinallyFunctions.SubMap
      "Code" -> λ(GLOBAL.ThenFinallyFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.padStart -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.padStart
      "Configurable" -> true
    }
    #GLOBAL.Promise[SYMBOL_species] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get [Symbol.species]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise[SYMBOL_species].SubMap
      "Code" -> λ(GLOBAL.Promise[SYMBOL_species])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.WeakMap.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.WeakMap.prototype
      "name" -> #DESC:GLOBAL.WeakMap.name
      "length" -> #DESC:GLOBAL.WeakMap.length
    }
    #GLOBAL.Map -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Map"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.SubMap
      "Code" -> λ(GLOBAL.Map)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.BigInt.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.BigInt.prototype[SYMBOL_toStringTag]
      "toString" -> #DESC:GLOBAL.BigInt.prototype.toString
      "valueOf" -> #DESC:GLOBAL.BigInt.prototype.valueOf
      "constructor" -> #DESC:GLOBAL.BigInt.prototype.constructor
    }
    #GLOBAL.Array.prototype.reduceRight.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.reduceRight.name
      "length" -> #DESC:GLOBAL.Array.prototype.reduceRight.length
    }
    #DESC:GLOBAL.ForInIteratorPrototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.keys -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "keys"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.keys.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.keys)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.charAt.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.charAt.name
      "length" -> #DESC:GLOBAL.String.prototype.charAt.length
    }
    #GLOBAL.Object.isExtensible.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.isExtensible.name
      "length" -> #DESC:GLOBAL.Object.isExtensible.length
    }
    #DESC:GLOBAL.Object.prototype.propertyIsEnumerable.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.WeakSet.prototype.has.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakSet.prototype.has.name
      "length" -> #DESC:GLOBAL.WeakSet.prototype.has.length
    }
    #DESC:GLOBAL.Number.isSafeInteger.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.assign.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.assign.name
      "length" -> #DESC:GLOBAL.Object.assign.length
    }
    #GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions.name
      "length" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions.length
    }
    #GLOBAL.String.prototype.replace.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.replace.name
      "length" -> #DESC:GLOBAL.String.prototype.replace.length
    }
    #DESC:GLOBAL.decodeURIComponent.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.indexOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "indexOf"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.substring -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "substring"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.substring.SubMap
      "Code" -> λ(GLOBAL.String.prototype.substring)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Function.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Function
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.toLocaleString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toLocaleString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.prototype.toLocaleString.SubMap
      "Code" -> λ(GLOBAL.Object.prototype.toLocaleString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.prototype.valueOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Symbol.prototype.valueOf.name
      "length" -> #DESC:GLOBAL.Symbol.prototype.valueOf.length
    }
    #GLOBAL.Set.prototype.values.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.values.name
      "length" -> #DESC:GLOBAL.Set.prototype.values.length
    }
    #GLOBAL.Map[SYMBOL_species].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map[SYMBOL_species].name
      "length" -> #DESC:GLOBAL.Map[SYMBOL_species].length
    }
    #55 -> (TYPE = ReferenceRecord) {
      "ThisValue" -> ~empty~
      "Base" -> N(#17)
      "Strict" -> true
      "ReferencedName" -> N("print")
    }
    #GLOBAL.Map.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.iterator -> #DESC:GLOBAL.Map.prototype[SYMBOL_iterator]
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.Map.prototype[SYMBOL_toStringTag]
      "get" -> #DESC:GLOBAL.Map.prototype.get
      "size" -> #DESC:GLOBAL.Map.prototype.size
      "delete" -> #DESC:GLOBAL.Map.prototype.delete
      "set" -> #DESC:GLOBAL.Map.prototype.set
      "forEach" -> #DESC:GLOBAL.Map.prototype.forEach
      "entries" -> #DESC:GLOBAL.Map.prototype.entries
      "has" -> #DESC:GLOBAL.Map.prototype.has
      "values" -> #DESC:GLOBAL.Map.prototype.values
      "clear" -> #DESC:GLOBAL.Map.prototype.clear
      "constructor" -> #DESC:GLOBAL.Map.prototype.constructor
      "keys" -> #DESC:GLOBAL.Map.prototype.keys
    }
    #DESC:GLOBAL.Array.prototype.flatMap -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.flatMap
      "Configurable" -> true
    }
    #GLOBAL.Number -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Number"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.SubMap
      "Code" -> λ(GLOBAL.Number)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.getPrototypeOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "getPrototypeOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.getPrototypeOf.SubMap
      "Code" -> λ(GLOBAL.Object.getPrototypeOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Number.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.WeakSet.prototype.add -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "add"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakSet.prototype.add.SubMap
      "Code" -> λ(GLOBAL.WeakSet.prototype.add)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Symbol.hasInstance -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.hasInstance
      "Configurable" -> false
    }
    #GLOBAL.PromiseRejectFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "PromiseRejectFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.PromiseRejectFunctions.SubMap
      "Code" -> λ(GLOBAL.PromiseRejectFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakMap.prototype.set.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "set"
      "Configurable" -> true
    }
    #GLOBAL.isFinite.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.isFinite.name
      "length" -> #DESC:GLOBAL.isFinite.length
    }
    #GLOBAL.IteratorPrototype[SYMBOL_iterator] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.iterator]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.IteratorPrototype[SYMBOL_iterator].SubMap
      "Code" -> λ(GLOBAL.IteratorPrototype[SYMBOL_iterator])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.push.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "push"
      "Configurable" -> true
    }
    #GLOBAL.Object.isFrozen -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isFrozen"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.isFrozen.SubMap
      "Code" -> λ(GLOBAL.Object.isFrozen)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.replaceAll.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "replaceAll"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.toLocaleLowerCase -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toLocaleLowerCase"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.toLocaleLowerCase.SubMap
      "Code" -> λ(GLOBAL.String.prototype.toLocaleLowerCase)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #11 -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #10
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.prototype.add -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.add
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.entries.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype[SYMBOL_toPrimitive].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.delete -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.delete
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.values.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "values"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorFunction.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncGeneratorFunction"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.every.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "every"
      "Configurable" -> true
    }
    #GLOBAL.Symbol.for -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "for"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.for.SubMap
      "Code" -> λ(GLOBAL.Symbol.for)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.prototype.toString.name
      "length" -> #DESC:GLOBAL.Object.prototype.toString.length
    }
    #DESC:GLOBAL.Number.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Number"
      "Configurable" -> true
    }
    #57 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.print
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.values -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "values"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Set.prototype.values.SubMap
      "Code" -> λ(GLOBAL.Set.prototype.values)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #56 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.print
      "Configurable" -> true
    }
    #GLOBAL.Float64Array -> (NotSupported "OrdinaryObject" "GLOBAL.Float64Array")
    #GLOBAL.Object.keys.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.keys.name
      "length" -> #DESC:GLOBAL.Object.keys.length
    }
    #DESC:GLOBAL.Array.prototype.filter.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #17 -> (TYPE = GlobalEnvironmentRecord) {
      "WithBaseObject" -> λ(GlobalEnvironmentRecord.WithBaseObject)
      "DeleteBinding" -> λ(GlobalEnvironmentRecord.DeleteBinding)
      "CreateMutableBinding" -> λ(GlobalEnvironmentRecord.CreateMutableBinding)
      "HasRestrictedGlobalProperty" -> λ(GlobalEnvironmentRecord.HasRestrictedGlobalProperty)
      "CreateGlobalFunctionBinding" -> λ(GlobalEnvironmentRecord.CreateGlobalFunctionBinding)
      "GetBindingValue" -> λ(GlobalEnvironmentRecord.GetBindingValue)
      "CreateGlobalVarBinding" -> λ(GlobalEnvironmentRecord.CreateGlobalVarBinding)
      "HasLexicalDeclaration" -> λ(GlobalEnvironmentRecord.HasLexicalDeclaration)
      "OuterEnv" -> null
      "VarNames" -> #18
      "HasSuperBinding" -> λ(GlobalEnvironmentRecord.HasSuperBinding)
      "GetThisBinding" -> λ(GlobalEnvironmentRecord.GetThisBinding)
      "CanDeclareGlobalFunction" -> λ(GlobalEnvironmentRecord.CanDeclareGlobalFunction)
      "DeclarativeRecord" -> #15
      "InitializeBinding" -> λ(GlobalEnvironmentRecord.InitializeBinding)
      "CreateImmutableBinding" -> λ(GlobalEnvironmentRecord.CreateImmutableBinding)
      "ObjectRecord" -> #13
      "HasThisBinding" -> λ(GlobalEnvironmentRecord.HasThisBinding)
      "SetMutableBinding" -> λ(GlobalEnvironmentRecord.SetMutableBinding)
      "HasBinding" -> λ(GlobalEnvironmentRecord.HasBinding)
      "CanDeclareGlobalVar" -> λ(GlobalEnvironmentRecord.CanDeclareGlobalVar)
      "GlobalThisValue" -> #11
      "SubMap" -> #16
      "HasVarDeclaration" -> λ(GlobalEnvironmentRecord.HasVarDeclaration)
    }
    #DESC:GLOBAL.Map.prototype.get -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.get
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.findIndex.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.findIndex.name
      "length" -> #DESC:GLOBAL.Array.prototype.findIndex.length
    }
    #1 -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.ThrowTypeError
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> #GLOBAL.ThrowTypeError
    }
    #DESC:GLOBAL.Object.prototype.propertyIsEnumerable.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "propertyIsEnumerable"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.lastIndexOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.lastIndexOf.name
      "length" -> #DESC:GLOBAL.String.prototype.lastIndexOf.length
    }
    #DESC:GLOBAL.Set.prototype[SYMBOL_iterator] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.values
      "Configurable" -> true
    }
    #GLOBAL.WeakMap.prototype.set.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakMap.prototype.set.name
      "length" -> #DESC:GLOBAL.WeakMap.prototype.set.length
    }
    #GLOBAL.Array.prototype.SubMap -> (TYPE = SubMap) {
      "splice" -> #DESC:GLOBAL.Array.prototype.splice
      "toString" -> #DESC:GLOBAL.Array.prototype.toString
      "join" -> #DESC:GLOBAL.Array.prototype.join
      #GLOBAL.Symbol.unscopables -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables]
      "sort" -> #DESC:GLOBAL.Array.prototype.sort
      "fill" -> #DESC:GLOBAL.Array.prototype.fill
      "find" -> #DESC:GLOBAL.Array.prototype.find
      "flatMap" -> #DESC:GLOBAL.Array.prototype.flatMap
      "some" -> #DESC:GLOBAL.Array.prototype.some
      "reverse" -> #DESC:GLOBAL.Array.prototype.reverse
      "every" -> #DESC:GLOBAL.Array.prototype.every
      "filter" -> #DESC:GLOBAL.Array.prototype.filter
      #GLOBAL.Symbol.iterator -> #DESC:GLOBAL.Array.prototype[SYMBOL_iterator]
      "values" -> #DESC:GLOBAL.Array.prototype.values
      "toLocaleString" -> #DESC:GLOBAL.Array.prototype.toLocaleString
      "slice" -> #DESC:GLOBAL.Array.prototype.slice
      "findIndex" -> #DESC:GLOBAL.Array.prototype.findIndex
      "shift" -> #DESC:GLOBAL.Array.prototype.shift
      "reduce" -> #DESC:GLOBAL.Array.prototype.reduce
      "includes" -> #DESC:GLOBAL.Array.prototype.includes
      "copyWithin" -> #DESC:GLOBAL.Array.prototype.copyWithin
      "flat" -> #DESC:GLOBAL.Array.prototype.flat
      "lastIndexOf" -> #DESC:GLOBAL.Array.prototype.lastIndexOf
      "length" -> #DESC:GLOBAL.Array.prototype.length
      "map" -> #DESC:GLOBAL.Array.prototype.map
      "pop" -> #DESC:GLOBAL.Array.prototype.pop
      "constructor" -> #DESC:GLOBAL.Array.prototype.constructor
      "keys" -> #DESC:GLOBAL.Array.prototype.keys
      "unshift" -> #DESC:GLOBAL.Array.prototype.unshift
      "reduceRight" -> #DESC:GLOBAL.Array.prototype.reduceRight
      "indexOf" -> #DESC:GLOBAL.Array.prototype.indexOf
      "concat" -> #DESC:GLOBAL.Array.prototype.concat
      "forEach" -> #DESC:GLOBAL.Array.prototype.forEach
      "push" -> #DESC:GLOBAL.Array.prototype.push
      "entries" -> #DESC:GLOBAL.Array.prototype.entries
    }
    #DESC:GLOBAL.String.prototype.toUpperCase.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toUpperCase"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.filter -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.filter
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "WeakSet"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.charCodeAt -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "charCodeAt"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.charCodeAt.SubMap
      "Code" -> λ(GLOBAL.String.prototype.charCodeAt)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.some -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.some
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.concat.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "concat"
      "Configurable" -> true
    }
    #DESC:GLOBAL.decodeURIComponent -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.decodeURIComponent
      "Configurable" -> true
    }
    #DESC:GLOBAL.IteratorPrototype[SYMBOL_iterator].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.seal.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "seal"
      "Configurable" -> true
    }
    #32 -> []
    #DESC:GLOBAL.BigInt.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.from.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "from"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.values -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.values
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.isExtensible.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isExtensible"
      "Configurable" -> true
    }
    #GLOBAL.WeakSet.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.WeakSet.prototype[SYMBOL_toStringTag]
      "delete" -> #DESC:GLOBAL.WeakSet.prototype.delete
      "constructor" -> #DESC:GLOBAL.WeakSet.prototype.constructor
      "add" -> #DESC:GLOBAL.WeakSet.prototype.add
      "has" -> #DESC:GLOBAL.WeakSet.prototype.has
    }
    #GLOBAL.AggregateError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.AggregateError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.clear.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype.call.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Function.prototype.call.name
      "length" -> #DESC:GLOBAL.Function.prototype.call.length
    }
    #GLOBAL.GeneratorFunction -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "GeneratorFunction"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.GeneratorFunction.SubMap
      "Code" -> λ(GLOBAL.GeneratorFunction)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.slice.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "slice"
      "Configurable" -> true
    }
    #DESC:GLOBAL.StringIteratorPrototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "String Iterator"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.has -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.has
      "Configurable" -> true
    }
    #GLOBAL.Promise.allSettled -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "allSettled"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.allSettled.SubMap
      "Code" -> λ(GLOBAL.Promise.allSettled)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.prototype.isPrototypeOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.prototype.isPrototypeOf.name
      "length" -> #DESC:GLOBAL.Object.prototype.isPrototypeOf.length
    }
    #DESC:GLOBAL.isFinite.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Boolean.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Error.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Error
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.isFrozen.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Generator.prototype.throw.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Generator.prototype.throw.name
      "length" -> #DESC:GLOBAL.Generator.prototype.throw.length
    }
    #DESC:GLOBAL.SetIteratorPrototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Set Iterator"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.isSafeInteger.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isSafeInteger"
      "Configurable" -> true
    }
    #GLOBAL.ForInIteratorPrototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ForInIteratorPrototype.next.name
      "length" -> #DESC:GLOBAL.ForInIteratorPrototype.next.length
    }
    #DESC:GLOBAL.Number.prototype.valueOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.prototype.valueOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.GeneratorFunction -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.GeneratorFunction
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.forEach -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.forEach
      "Configurable" -> true
    }
    #GLOBAL.parseFloat.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.parseFloat.name
      "length" -> #DESC:GLOBAL.parseFloat.length
    }
    #DESC:GLOBAL.Array.prototype.findIndex -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.findIndex
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.defineProperty.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 3.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.of.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "of"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.copyWithin -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.copyWithin
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.charCodeAt -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.charCodeAt
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.indexOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Boolean.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.Boolean.prototype
      "name" -> #DESC:GLOBAL.Boolean.name
      "length" -> #DESC:GLOBAL.Boolean.length
    }
    #DESC:GLOBAL.Number.prototype.toLocaleString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toLocaleString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.toString
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.entries.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "entries"
      "Configurable" -> true
    }
    #REALM -> (TYPE = RealmRecord) {
      "TemplateMap" -> #7
      "GlobalObject" -> #11
      "GlobalEnv" -> N(#17)
      "Intrinsics" -> #INTRINSICS
      "SubMap" -> #REALM.SubMap
    }
    #DESC:GLOBAL.Promise.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise
      "Configurable" -> true
    }
    #GLOBAL.EvalError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "EvalError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.EvalError.SubMap
      "Code" -> λ(GLOBAL.EvalError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.isExtensible -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.isExtensible
      "Configurable" -> true
    }
    #DESC:GLOBAL.TypeError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "TypeError"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.slice.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.slice.name
      "length" -> #DESC:GLOBAL.Array.prototype.slice.length
    }
    #DESC:GLOBAL.ArgGetter -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ArgGetter
      "Configurable" -> true
    }
    #GLOBAL.JSON -> (NotSupported "OrdinaryObject" "GLOBAL.JSON")
    #GLOBAL.ReferenceError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "ReferenceError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ReferenceError.SubMap
      "Code" -> λ(GLOBAL.ReferenceError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.prototype.size -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Set.prototype.size
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #DESC:GLOBAL.Object.getOwnPropertyDescriptors.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.AsyncIteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.AsyncGenerator.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ArgSetter.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "ArgSetter"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.bind.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "bind"
      "Configurable" -> true
    }
    #GLOBAL.MapIteratorPrototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.MapIteratorPrototype.next.name
      "length" -> #DESC:GLOBAL.MapIteratorPrototype.next.length
    }
    #GLOBAL.StringIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.IteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.StringIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise.any -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "any"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.any.SubMap
      "Code" -> λ(GLOBAL.Promise.any)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.getOwnPropertyNames -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.getOwnPropertyNames
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.toUpperCase -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toUpperCase"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.toUpperCase.SubMap
      "Code" -> λ(GLOBAL.String.prototype.toUpperCase)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #44 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #GLOBAL.Array.prototype.join -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "join"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.join.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.join)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Map.prototype.size.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.keys.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "keys"
      "Configurable" -> true
    }
    #GLOBAL.SubMap -> (TYPE = SubMap) {
      "print" -> #DESC:GLOBAL.print
      "Boolean" -> #DESC:GLOBAL.Boolean
      "undefined" -> #DESC:GLOBAL.undefined
      "ArgGetter" -> #DESC:GLOBAL.ArgGetter
      "AwaitFulfilledFunctions" -> #DESC:GLOBAL.AwaitFulfilledFunctions
      "isFinite" -> #DESC:GLOBAL.isFinite
      "PromiseResolveFunctions" -> #DESC:GLOBAL.PromiseResolveFunctions
      "$262" -> #DESC:GLOBAL.$262
      "Uint8Array" -> #DESC:GLOBAL.Uint8Array
      "parseInt" -> #DESC:GLOBAL.parseInt
      "Function" -> #DESC:GLOBAL.Function
      "FinalizationRegistry" -> #DESC:GLOBAL.FinalizationRegistry
      "encodeURI" -> #DESC:GLOBAL.encodeURI
      "BigInt64Array" -> #DESC:GLOBAL.BigInt64Array
      "Atomics" -> #DESC:GLOBAL.Atomics
      "Promise" -> #DESC:GLOBAL.Promise
      "Uint32Array" -> #DESC:GLOBAL.Uint32Array
      "decodeURIComponent" -> #DESC:GLOBAL.decodeURIComponent
      "ArrayBuffer" -> #DESC:GLOBAL.ArrayBuffer
      "encodeURIComponent" -> #DESC:GLOBAL.encodeURIComponent
      "GetCapabilitiesExecutorFunctions" -> #DESC:GLOBAL.GetCapabilitiesExecutorFunctions
      "SharedArrayBuffer" -> #DESC:GLOBAL.SharedArrayBuffer
      "IfAbruptRejectPromise" -> #DESC:GLOBAL.IfAbruptRejectPromise
      "Math" -> #DESC:GLOBAL.Math
      "TypedArray" -> #DESC:GLOBAL.TypedArray
      "BigUint64Array" -> #DESC:GLOBAL.BigUint64Array
      "BigInt" -> #DESC:GLOBAL.BigInt
      "Uint8ClampedArray" -> #DESC:GLOBAL.Uint8ClampedArray
      "NaN" -> #DESC:GLOBAL.NaN
      "isNaN" -> #DESC:GLOBAL.isNaN
      "JSON" -> #DESC:GLOBAL.JSON
      "globalThis" -> #DESC:GLOBAL.globalThis
      "Infinity" -> #DESC:GLOBAL.Infinity
      "PromiseRejectFunctions" -> #DESC:GLOBAL.PromiseRejectFunctions
      "WeakMap" -> #DESC:GLOBAL.WeakMap
      "AggregateError" -> #DESC:GLOBAL.AggregateError
      "RangeError" -> #DESC:GLOBAL.RangeError
      "Int8Array" -> #DESC:GLOBAL.Int8Array
      "AsyncfromSyncIteratorValueUnwrapFunctions" -> #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions
      "Uint16Array" -> #DESC:GLOBAL.Uint16Array
      "decodeURI" -> #DESC:GLOBAL.decodeURI
      "DefaultConstructorFunctions" -> #DESC:GLOBAL.DefaultConstructorFunctions
      "AsyncGeneratorResumeNextReturnProcessorRejectedFunctions" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions
      "Reflect" -> #DESC:GLOBAL.Reflect
      "Number" -> #DESC:GLOBAL.Number
      "RegExp" -> #DESC:GLOBAL.RegExp
      "Symbol" -> #DESC:GLOBAL.Symbol
      "SyntaxError" -> #DESC:GLOBAL.SyntaxError
      "AsyncGeneratorFunction" -> #DESC:GLOBAL.AsyncGeneratorFunction
      "ProxyRevocationFunctions" -> #DESC:GLOBAL.ProxyRevocationFunctions
      "GeneratorFunction" -> #DESC:GLOBAL.GeneratorFunction
      "TypeError" -> #DESC:GLOBAL.TypeError
      "Proxy" -> #DESC:GLOBAL.Proxy
      "InternalizeJSONProperty" -> #DESC:GLOBAL.InternalizeJSONProperty
      "eval" -> #DESC:GLOBAL.eval
      "CatchFinallyFunctions" -> #DESC:GLOBAL.CatchFinallyFunctions
      "ThrowTypeError" -> #DESC:GLOBAL.ThrowTypeError
      "DataView" -> #DESC:GLOBAL.DataView
      "parseFloat" -> #DESC:GLOBAL.parseFloat
      "Set" -> #DESC:GLOBAL.Set
      "Float32Array" -> #DESC:GLOBAL.Float32Array
      "ThenFinallyFunctions" -> #DESC:GLOBAL.ThenFinallyFunctions
      "AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions
      "Error" -> #DESC:GLOBAL.Error
      "WeakSet" -> #DESC:GLOBAL.WeakSet
      "EvalError" -> #DESC:GLOBAL.EvalError
      "AwaitRejectedFunctions" -> #DESC:GLOBAL.AwaitRejectedFunctions
      "Int32Array" -> #DESC:GLOBAL.Int32Array
      "URIError" -> #DESC:GLOBAL.URIError
      "String" -> #DESC:GLOBAL.String
      "Object" -> #DESC:GLOBAL.Object
      "Float64Array" -> #DESC:GLOBAL.Float64Array
      "Date" -> #DESC:GLOBAL.Date
      "Array" -> #DESC:GLOBAL.Array
      "Map" -> #DESC:GLOBAL.Map
      "Int16Array" -> #DESC:GLOBAL.Int16Array
      "__ABS__" -> #DESC:GLOBAL.__ABS__
      "HostPrint" -> #DESC:GLOBAL.HostPrint
      "ReferenceError" -> #DESC:GLOBAL.ReferenceError
      "CreateDataPropertyOnObjectFunctions" -> #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions
      "ArgSetter" -> #DESC:GLOBAL.ArgSetter
    }
    #DESC:GLOBAL.Function.prototype.apply.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "apply"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.EPSILON -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.220446049250313E-16
      "Configurable" -> false
    }
    #GLOBAL.Number.prototype.toExponential.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.prototype.toExponential.name
      "length" -> #DESC:GLOBAL.Number.prototype.toExponential.length
    }
    #GLOBAL.DefaultConstructorFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.DefaultConstructorFunctions.name
      "length" -> #DESC:GLOBAL.DefaultConstructorFunctions.length
    }
    #DESC:GLOBAL.Generator.prototype.return.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "return"
      "Configurable" -> true
    }
    #GLOBAL.Symbol.split -> (Symbol "Symbol.split")
    #DESC:GLOBAL.IfAbruptRejectPromise -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.IfAbruptRejectPromise
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Function.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.lastIndexOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.toStringTag -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.toStringTag
      "Configurable" -> false
    }
    #DESC:GLOBAL.Array.prototype.entries.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.assign.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype[SYMBOL_hasInstance].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.TypeError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.TypeError.prototype
      "name" -> #DESC:GLOBAL.TypeError.name
      "length" -> #DESC:GLOBAL.TypeError.length
    }
    #25 -> (TYPE = ExecutionContext) {
      "Function" -> null
      "Realm" -> #REALM
      "LexicalEnvironment" -> N(#17)
      "ScriptOrModule" -> N(#24)
      "VariableEnvironment" -> N(#17)
    }
    #DESC:GLOBAL.Set.prototype.entries -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.entries
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype[SYMBOL_toPrimitive].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Symbol.prototype[SYMBOL_toPrimitive].name
      "length" -> #DESC:GLOBAL.Symbol.prototype[SYMBOL_toPrimitive].length
    }
    #DESC:GLOBAL.GeneratorFunction.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.GeneratorFunction.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.BigInt.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt.prototype.toString
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions"
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.clear.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.clear.name
      "length" -> #DESC:GLOBAL.Map.prototype.clear.length
    }
    #DESC:GLOBAL.String.prototype.match -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.match
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.values.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "values"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.forEach.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.repeat -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "repeat"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.repeat.SubMap
      "Code" -> λ(GLOBAL.String.prototype.repeat)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakSet.prototype.add.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Symbol.keyFor.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Symbol.keyFor.name
      "length" -> #DESC:GLOBAL.Symbol.keyFor.length
    }
    #GLOBAL.IteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.IteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Set.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Set.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.BigUint64Array -> (NotSupported "OrdinaryObject" "GLOBAL.BigUint64Array")
    #DESC:GLOBAL.Float64Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Float64Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.match.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "match"
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.toExponential -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toExponential"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.prototype.toExponential.SubMap
      "Code" -> λ(GLOBAL.Number.prototype.toExponential)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map.prototype.entries -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "entries"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.entries.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.entries)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Generator.prototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.valueOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype -> (TYPE = ImmutablePrototypeExoticObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(ImmutablePrototypeExoticObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> null
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Object.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.toLowerCase -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.toLowerCase
      "Configurable" -> true
    }
    #DESC:GLOBAL.eval -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.eval
      "Configurable" -> true
    }
    #GLOBAL.AsyncFunction.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.AsyncFunction.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Set.prototype.forEach.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "forEach"
      "Configurable" -> true
    }
    #15 -> (TYPE = DeclarativeEnvironmentRecord) {
      "InitializeBinding" -> λ(DeclarativeEnvironmentRecord.InitializeBinding)
      "WithBaseObject" -> λ(DeclarativeEnvironmentRecord.WithBaseObject)
      "DeleteBinding" -> λ(DeclarativeEnvironmentRecord.DeleteBinding)
      "CreateImmutableBinding" -> λ(DeclarativeEnvironmentRecord.CreateImmutableBinding)
      "CreateMutableBinding" -> λ(DeclarativeEnvironmentRecord.CreateMutableBinding)
      "GetBindingValue" -> λ(DeclarativeEnvironmentRecord.GetBindingValue)
      "HasBinding" -> λ(DeclarativeEnvironmentRecord.HasBinding)
      "SubMap" -> #14
      "HasSuperBinding" -> λ(DeclarativeEnvironmentRecord.HasSuperBinding)
      "HasThisBinding" -> λ(DeclarativeEnvironmentRecord.HasThisBinding)
      "SetMutableBinding" -> λ(DeclarativeEnvironmentRecord.SetMutableBinding)
    }
    #DESC:GLOBAL.Generator.prototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Generator.prototype.next
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.valueOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "valueOf"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype.throw -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "throw"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncGenerator.prototype.throw.SubMap
      "Code" -> λ(GLOBAL.AsyncGenerator.prototype.throw)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Uint16Array -> (NotSupported "OrdinaryObject" "GLOBAL.Uint16Array")
    #DESC:GLOBAL.RangeError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "String"
      "Configurable" -> true
    }
    #GLOBAL.Object.getOwnPropertyDescriptor.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.getOwnPropertyDescriptor.name
      "length" -> #DESC:GLOBAL.Object.getOwnPropertyDescriptor.length
    }
    #GLOBAL.Promise.prototype.then.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.prototype.then.name
      "length" -> #DESC:GLOBAL.Promise.prototype.then.length
    }
    #GLOBAL.ArrayIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.IteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.ArrayIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].flatMap -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.replace -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "replace"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.replace.SubMap
      "Code" -> λ(GLOBAL.String.prototype.replace)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Function -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Function
      "Configurable" -> true
    }
    #GLOBAL.Boolean -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Boolean"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Boolean.SubMap
      "Code" -> λ(GLOBAL.Boolean)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map.prototype.delete.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.delete.name
      "length" -> #DESC:GLOBAL.Map.prototype.delete.length
    }
    #GLOBAL.WeakRef -> (NotSupported "OrdinaryObject" "GLOBAL.WeakRef")
    #DESC:GLOBAL.Number.prototype.toFixed.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toFixed"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Uint16Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Uint16Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.isArray.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isArray"
      "Configurable" -> true
    }
    #DESC:GLOBAL.URIError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.URIError
      "Configurable" -> true
    }
    #DESC:GLOBAL.TypedArray[SYMBOL_species].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.species]"
      "Configurable" -> true
    }
    #GLOBAL -> (TYPE = Map) {
      "SubMap" -> #GLOBAL.SubMap
    }
    #DESC:GLOBAL.Array.prototype.flat.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "flat"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.setPrototypeOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.setPrototypeOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.AwaitFulfilledFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Error.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Error.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Error.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.getOwnPropertySymbols -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.getOwnPropertySymbols
      "Configurable" -> true
    }
    #DESC:GLOBAL.RangeError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.RangeError
      "Configurable" -> true
    }
    #22 -> (TYPE = ExecutionContext) {
      "Function" -> null
      "ScriptOrModule" -> null
      "Realm" -> N(#REALM)
      "SubMap" -> #23
    }
    #DESC:GLOBAL.Object.isSealed -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.isSealed
      "Configurable" -> true
    }
    #GLOBAL.StringIteratorPrototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.StringIteratorPrototype.next.name
      "length" -> #DESC:GLOBAL.StringIteratorPrototype.next.length
    }
    #DESC:GLOBAL.AwaitRejectedFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AwaitRejectedFunctions"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype.throw.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncGenerator.prototype.throw.name
      "length" -> #DESC:GLOBAL.AsyncGenerator.prototype.throw.length
    }
    #GLOBAL.WeakMap -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "WeakMap"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakMap.SubMap
      "Code" -> λ(GLOBAL.WeakMap)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.concat -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "concat"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.concat.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.concat)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.match -> (Symbol "Symbol.match")
    #DESC:GLOBAL.TypedArray -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.TypedArray
      "Configurable" -> true
    }
    #GLOBAL.FinalizationRegistry.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.FinalizationRegistry.name
      "length" -> #DESC:GLOBAL.FinalizationRegistry.length
    }
    #DESC:GLOBAL.BigInt.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "BigInt"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.is.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.defineProperties -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.defineProperties
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions
      "Configurable" -> true
    }
    #GLOBAL.Promise.prototype.catch -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "catch"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.prototype.catch.SubMap
      "Code" -> λ(GLOBAL.Promise.prototype.catch)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.AggregateError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #GLOBAL.ArgGetter -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "ArgGetter"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ArgGetter.SubMap
      "Code" -> λ(GLOBAL.ArgGetter)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.matchAll.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.isPrototypeOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Promise.prototype.SubMap -> (TYPE = SubMap) {
      "finally" -> #DESC:GLOBAL.Promise.prototype.finally
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.Promise.prototype[SYMBOL_toStringTag]
      "catch" -> #DESC:GLOBAL.Promise.prototype.catch
      "constructor" -> #DESC:GLOBAL.Promise.prototype.constructor
      "then" -> #DESC:GLOBAL.Promise.prototype.then
    }
    #GLOBAL.Number.prototype.valueOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "valueOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.prototype.valueOf.SubMap
      "Code" -> λ(GLOBAL.Number.prototype.valueOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.reduce -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.reduce
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.padEnd -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "padEnd"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.padEnd.SubMap
      "Code" -> λ(GLOBAL.String.prototype.padEnd)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.species -> (Symbol "Symbol.species")
    #GLOBAL.WeakSet.prototype.add.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakSet.prototype.add.name
      "length" -> #DESC:GLOBAL.WeakSet.prototype.add.length
    }
    #DESC:GLOBAL.Array.isArray.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.throw.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.IteratorPrototype[SYMBOL_iterator].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.IteratorPrototype[SYMBOL_iterator].name
      "length" -> #DESC:GLOBAL.IteratorPrototype[SYMBOL_iterator].length
    }
    #GLOBAL.EvalError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.EvalError.prototype
      "name" -> #DESC:GLOBAL.EvalError.name
      "length" -> #DESC:GLOBAL.EvalError.length
    }
    #GLOBAL.AsyncGeneratorFunction.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.AsyncGeneratorFunction.prototype
      "name" -> #DESC:GLOBAL.AsyncGeneratorFunction.name
      "length" -> #DESC:GLOBAL.AsyncGeneratorFunction.length
    }
    #DESC:GLOBAL.ArgSetter.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "WeakMap"
      "Configurable" -> true
    }
    #DESC:GLOBAL.TypedArray.from.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #41 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #DESC:GLOBAL.TypeError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.TypeError
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.charAt -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.charAt
      "Configurable" -> true
    }
    #DESC:GLOBAL.HostPrint.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "HostPrint"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype[SYMBOL_unscopables].SubMap -> (TYPE = SubMap) {
      "values" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].values
      "findIndex" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].findIndex
      "fill" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].fill
      "length" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].length
      "keys" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].keys
      "find" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].find
      "flatMap" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].flatMap
      "entries" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].entries
      "name" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].name
      "includes" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].includes
      "copyWithin" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].copyWithin
      "flat" -> #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].flat
    }
    #DESC:GLOBAL.Promise.race.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.SubMap -> (TYPE = SubMap) {
      "toString" -> #DESC:GLOBAL.Number.prototype.toString
      "toExponential" -> #DESC:GLOBAL.Number.prototype.toExponential
      "constructor" -> #DESC:GLOBAL.Number.prototype.constructor
      "toPrecision" -> #DESC:GLOBAL.Number.prototype.toPrecision
      "valueOf" -> #DESC:GLOBAL.Number.prototype.valueOf
      "toLocaleString" -> #DESC:GLOBAL.Number.prototype.toLocaleString
      "toFixed" -> #DESC:GLOBAL.Number.prototype.toFixed
    }
    #DESC:GLOBAL.Generator.prototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Symbol.toStringTag -> (Symbol "Symbol.toStringTag")
    #GLOBAL.Error.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Error.prototype.toString.name
      "length" -> #DESC:GLOBAL.Error.prototype.toString.length
    }
    #DESC:GLOBAL.Set.prototype.has -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.has
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.all -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.all
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions
      "Configurable" -> true
    }
    #GLOBAL.Boolean.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Boolean.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Boolean.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.flatMap.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.clear.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.size.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> 0.0
      "Configurable" -> false
    }
    #DESC:GLOBAL.Object.prototype.toLocaleString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.prototype.toLocaleString
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.replaceAll -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "replaceAll"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.replaceAll.SubMap
      "Code" -> λ(GLOBAL.String.prototype.replaceAll)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.WeakMap.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.WeakMap.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.MapIteratorPrototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Promise.all -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "all"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.all.SubMap
      "Code" -> λ(GLOBAL.Promise.all)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.create -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.create
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array[SYMBOL_species].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get [Symbol.species]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.EvalError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "EvalError"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.toString -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toString"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.toString.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.toString)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.reject -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.reject
      "Configurable" -> true
    }
    #DESC:GLOBAL.URIError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "URIError"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.forEach.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.isInteger.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.CreateDataPropertyOnObjectFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getOwnPropertySymbols.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "getOwnPropertySymbols"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.isNaN.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isNaN"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.keys -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "keys"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.keys.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.keys)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.matchAll -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.matchAll
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.delete.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "delete"
      "Configurable" -> true
    }
    #30 -> [☊[VariableDeclaration](x = 1 + 2)]
    #DESC:GLOBAL.Number.prototype.toPrecision.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.parseInt -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "parseInt"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.parseInt.SubMap
      "Code" -> λ(GLOBAL.parseInt)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #8 -> (TYPE = ExecutionContext) {
      "Function" -> null
      "ScriptOrModule" -> null
      "Realm" -> N(#REALM)
    }
    #DESC:GLOBAL.SetIteratorPrototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype.bind -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "bind"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.prototype.bind.SubMap
      "Code" -> λ(GLOBAL.Function.prototype.bind)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.slice.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.BigInt.asIntN.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.BigInt.asIntN.name
      "length" -> #DESC:GLOBAL.BigInt.asIntN.length
    }
    #GLOBAL.TypeError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.TypeError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Boolean.prototype.valueOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "valueOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Boolean.prototype.valueOf.SubMap
      "Code" -> λ(GLOBAL.Boolean.prototype.valueOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Error.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Error.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Error.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.Error.prototype
      "name" -> #DESC:GLOBAL.Error.name
      "length" -> #DESC:GLOBAL.Error.length
    }
    #DESC:GLOBAL.ArrayIteratorPrototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Array Iterator"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.isFinite -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.isFinite
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.forEach.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "forEach"
      "Configurable" -> true
    }
    #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "CreateDataPropertyOnObjectFunctions"
      "Configurable" -> true
    }
    #GLOBAL.StringIteratorPrototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.StringIteratorPrototype[SYMBOL_toStringTag]
      "next" -> #DESC:GLOBAL.StringIteratorPrototype.next
    }
    #GLOBAL.Object.prototype.hasOwnProperty -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "hasOwnProperty"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.prototype.hasOwnProperty.SubMap
      "Code" -> λ(GLOBAL.Object.prototype.hasOwnProperty)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.includes -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.includes
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.includes.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.padEnd.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "padEnd"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.flatMap.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.flatMap.name
      "length" -> #DESC:GLOBAL.Array.prototype.flatMap.length
    }
    #DESC:GLOBAL.Symbol.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #GLOBAL.ArgSetter.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ArgSetter.name
      "length" -> #DESC:GLOBAL.ArgSetter.length
    }
    #DESC:GLOBAL.Symbol.for.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "for"
      "Configurable" -> true
    }
    #DESC:GLOBAL.FinalizationRegistry -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.FinalizationRegistry
      "Configurable" -> true
    }
    #53 -> ["Value"]
    #GLOBAL.SyntaxError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.SyntaxError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.unshift.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "unshift"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.raw -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.raw
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.prototype.toString
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.matchAll.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.matchAll.name
      "length" -> #DESC:GLOBAL.String.prototype.matchAll.length
    }
    #GLOBAL.Function -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Function"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.SubMap
      "Code" -> λ(GLOBAL.Function)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.reverse.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "reverse"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.return -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncFromSyncIteratorPrototype.return
      "Configurable" -> true
    }
    #DESC:GLOBAL.eval.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "eval"
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.entries.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.entries.name
      "length" -> #DESC:GLOBAL.Array.prototype.entries.length
    }
    #DESC:GLOBAL.AggregateError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "AggregateError"
      "Configurable" -> true
    }
    #9 -> ["Prototype", "Extensible"]
    #DESC:GLOBAL.String.prototype.search.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Symbol.unscopables -> (Symbol "Symbol.unscopables")
    #DESC:GLOBAL.Function.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Function"
      "Configurable" -> true
    }
    #GLOBAL.FinalizationRegistry -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "FinalizationRegistry"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.FinalizationRegistry.SubMap
      "Code" -> λ(GLOBAL.FinalizationRegistry)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakMap.prototype.set.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.forEach.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "forEach"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.concat.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.URIError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.URIError.prototype.name
      "constructor" -> #DESC:GLOBAL.URIError.prototype.constructor
      "message" -> #DESC:GLOBAL.URIError.prototype.message
    }
    #GLOBAL.Set.prototype.delete.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.delete.name
      "length" -> #DESC:GLOBAL.Set.prototype.delete.length
    }
    #GLOBAL.String.prototype.includes -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "includes"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.includes.SubMap
      "Code" -> λ(GLOBAL.String.prototype.includes)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.defineProperty.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.defineProperty.name
      "length" -> #DESC:GLOBAL.Object.defineProperty.length
    }
    #DESC:GLOBAL.Set.prototype.delete.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.push -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.push
      "Configurable" -> true
    }
    #50 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #DESC:GLOBAL.Array.prototype.pop.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Generator.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.Generator.prototype[SYMBOL_toStringTag]
      "return" -> #DESC:GLOBAL.Generator.prototype.return
      "constructor" -> #DESC:GLOBAL.Generator.prototype.constructor
      "throw" -> #DESC:GLOBAL.Generator.prototype.throw
      "next" -> #DESC:GLOBAL.Generator.prototype.next
    }
    #DESC:GLOBAL.String.prototype.slice -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.slice
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.indexOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.indexOf.name
      "length" -> #DESC:GLOBAL.String.prototype.indexOf.length
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.return.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "return"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.find -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "find"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.find.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.find)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.charAt -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "charAt"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.charAt.SubMap
      "Code" -> λ(GLOBAL.String.prototype.charAt)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.ThrowTypeError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "ThrowTypeError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ThrowTypeError.SubMap
      "Code" -> λ(GLOBAL.ThrowTypeError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> false
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.split -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "split"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.split.SubMap
      "Code" -> λ(GLOBAL.String.prototype.split)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.padEnd.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.isArray -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.isArray
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.keyFor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Symbol.keyFor
      "Configurable" -> true
    }
    #DESC:GLOBAL.AggregateError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AggregateError
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.resolve -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.resolve
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.split -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.split
      "Configurable" -> false
    }
    #DESC:GLOBAL.Object.getOwnPropertyDescriptor.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.unscopables]"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.push.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.push.name
      "length" -> #DESC:GLOBAL.Array.prototype.push.length
    }
    #DESC:GLOBAL.Error.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Error"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.split.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.split.name
      "length" -> #DESC:GLOBAL.String.prototype.split.length
    }
    #GLOBAL.Promise.prototype.then -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "then"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.prototype.then.SubMap
      "Code" -> λ(GLOBAL.Promise.prototype.then)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.ProxyRevocationFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ProxyRevocationFunctions.name
      "length" -> #DESC:GLOBAL.ProxyRevocationFunctions.length
    }
    #DESC:GLOBAL.Object.prototype.valueOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Boolean
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].copyWithin -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.ThrowTypeError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> false
    }
    #DESC:GLOBAL.Set.prototype.add.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.trimStart -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "trimStart"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.trimStart.SubMap
      "Code" -> λ(GLOBAL.String.prototype.trimStart)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.TypedArray.of.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.find.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.find.name
      "length" -> #DESC:GLOBAL.Array.prototype.find.length
    }
    #DESC:GLOBAL.Promise.all.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "all"
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.endsWith -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "endsWith"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.endsWith.SubMap
      "Code" -> λ(GLOBAL.String.prototype.endsWith)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.splice.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "splice"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getPrototypeOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.getPrototypeOf
      "Configurable" -> true
    }
    #0 -> (TYPE = Record) {}
    #DESC:GLOBAL.String.prototype.toUpperCase.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.trim.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "trim"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorFunction.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncGeneratorFunction"
      "Configurable" -> true
    }
    #GLOBAL.SetIteratorPrototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.SetIteratorPrototype.next.SubMap
      "Code" -> λ(GLOBAL.SetIteratorPrototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.reduce.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.replace -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.replace
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.shift -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.shift
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype[SYMBOL_hasInstance] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.hasInstance]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Function.prototype[SYMBOL_hasInstance].SubMap
      "Code" -> λ(GLOBAL.Function.prototype[SYMBOL_hasInstance])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.includes -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "includes"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.includes.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.includes)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.isFrozen.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isFrozen"
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.forEach.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.forEach.name
      "length" -> #DESC:GLOBAL.Set.prototype.forEach.length
    }
    #DESC:GLOBAL.Array.prototype.some.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.prototype.finally -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.prototype.finally
      "Configurable" -> true
    }
    #DESC:GLOBAL.URIError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #GLOBAL.BigInt.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.BigInt.prototype.toString.name
      "length" -> #DESC:GLOBAL.BigInt.prototype.toString.length
    }
    #DESC:GLOBAL.String.prototype.substring -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.substring
      "Configurable" -> true
    }
    #DESC:GLOBAL.PromiseRejectFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.PromiseRejectFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.keyFor.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakMap
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.splice -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "splice"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.splice.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.splice)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ArgSetter -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ArgSetter
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.String.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.CatchFinallyFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "CatchFinallyFunctions"
      "Configurable" -> true
    }
    #GLOBAL.Boolean.prototype.valueOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Boolean.prototype.valueOf.name
      "length" -> #DESC:GLOBAL.Boolean.prototype.valueOf.length
    }
    #DESC:GLOBAL.Promise.resolve.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "resolve"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ArrayBuffer -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ArrayBuffer
      "Configurable" -> true
    }
    #GLOBAL.Boolean.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "BooleanData" -> false
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Boolean.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.RegExp -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.RegExp
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.caller -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.ThrowTypeError
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> #GLOBAL.ThrowTypeError
    }
    #GLOBAL.ForInIteratorPrototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ForInIteratorPrototype.next.SubMap
      "Code" -> λ(GLOBAL.ForInIteratorPrototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.codePointAt.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.codePointAt.name
      "length" -> #DESC:GLOBAL.String.prototype.codePointAt.length
    }
    #DESC:GLOBAL.Number.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.asIntN -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt.asIntN
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.fill -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.fill
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.trimStart.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "trimStart"
      "Configurable" -> true
    }
    #GLOBAL.MapIteratorPrototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.MapIteratorPrototype[SYMBOL_toStringTag]
      "next" -> #DESC:GLOBAL.MapIteratorPrototype.next
    }
    #26 -> []
    #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncGeneratorResumeNextReturnProcessorRejectedFunctions"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.asyncIterator -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.asyncIterator
      "Configurable" -> false
    }
    #DESC:GLOBAL.TypedArray[SYMBOL_species] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.TypedArray[SYMBOL_species]
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.join -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.join
      "Configurable" -> true
    }
    #GLOBAL.TypedArray -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "TypedArray"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.TypedArray.SubMap
      "Code" -> λ(GLOBAL.TypedArray)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Function.prototype.bind -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Function.prototype.bind
      "Configurable" -> true
    }
    #DESC:GLOBAL.isNaN.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.join.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.join.name
      "length" -> #DESC:GLOBAL.Array.prototype.join.length
    }
    #DESC:GLOBAL.String.prototype[SYMBOL_iterator].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakSet
      "Configurable" -> true
    }
    #GLOBAL.Object.getOwnPropertyDescriptors.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.getOwnPropertyDescriptors.name
      "length" -> #DESC:GLOBAL.Object.getOwnPropertyDescriptors.length
    }
    #DESC:GLOBAL.String.prototype.lastIndexOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.lastIndexOf
      "Configurable" -> true
    }
    #GLOBAL.encodeURIComponent -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "encodeURIComponent"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.encodeURIComponent.SubMap
      "Code" -> λ(GLOBAL.encodeURIComponent)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.fromCodePoint.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Uint8Array -> (NotSupported "OrdinaryObject" "GLOBAL.Uint8Array")
    #DESC:GLOBAL.Object.isSealed.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.isPrototypeOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.prototype.isPrototypeOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.PromiseResolveFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.PromiseResolveFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.prototype.has -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakSet.prototype.has
      "Configurable" -> true
    }
    #23 -> (TYPE = SubMap) {}
    #GLOBAL.Array.prototype.findIndex -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "findIndex"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.findIndex.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.findIndex)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.PromiseResolveFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "PromiseResolveFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.PromiseResolveFunctions.SubMap
      "Code" -> λ(GLOBAL.PromiseResolveFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.padStart.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.WeakMap.prototype.delete -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "delete"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakMap.prototype.delete.SubMap
      "Code" -> λ(GLOBAL.WeakMap.prototype.delete)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.AsyncFromSyncIteratorPrototype.throw -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "throw"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncFromSyncIteratorPrototype.throw.SubMap
      "Code" -> λ(GLOBAL.AsyncFromSyncIteratorPrototype.throw)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Promise.SubMap -> (TYPE = SubMap) {
      "any" -> #DESC:GLOBAL.Promise.any
      "prototype" -> #DESC:GLOBAL.Promise.prototype
      "all" -> #DESC:GLOBAL.Promise.all
      #GLOBAL.Symbol.species -> #DESC:GLOBAL.Promise[SYMBOL_species]
      "resolve" -> #DESC:GLOBAL.Promise.resolve
      "name" -> #DESC:GLOBAL.Promise.name
      "allSettled" -> #DESC:GLOBAL.Promise.allSettled
      "race" -> #DESC:GLOBAL.Promise.race
      "length" -> #DESC:GLOBAL.Promise.length
      "reject" -> #DESC:GLOBAL.Promise.reject
    }
    #DESC:GLOBAL.Error.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.copyWithin.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.propertyIsEnumerable.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.prototype.propertyIsEnumerable.name
      "length" -> #DESC:GLOBAL.Object.prototype.propertyIsEnumerable.length
    }
    #GLOBAL.RangeError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "RangeError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.RangeError.SubMap
      "Code" -> λ(GLOBAL.RangeError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #10 -> (TYPE = SubMap) {
      "print" -> #DESC:GLOBAL.print
      "Boolean" -> #DESC:GLOBAL.Boolean
      "undefined" -> #DESC:GLOBAL.undefined
      "ArgGetter" -> #DESC:GLOBAL.ArgGetter
      "AwaitFulfilledFunctions" -> #DESC:GLOBAL.AwaitFulfilledFunctions
      "isFinite" -> #DESC:GLOBAL.isFinite
      "PromiseResolveFunctions" -> #DESC:GLOBAL.PromiseResolveFunctions
      "$262" -> #DESC:GLOBAL.$262
      "Uint8Array" -> #DESC:GLOBAL.Uint8Array
      "parseInt" -> #DESC:GLOBAL.parseInt
      "Function" -> #DESC:GLOBAL.Function
      "FinalizationRegistry" -> #DESC:GLOBAL.FinalizationRegistry
      "encodeURI" -> #DESC:GLOBAL.encodeURI
      "BigInt64Array" -> #DESC:GLOBAL.BigInt64Array
      "Atomics" -> #DESC:GLOBAL.Atomics
      "Promise" -> #DESC:GLOBAL.Promise
      "Uint32Array" -> #DESC:GLOBAL.Uint32Array
      "decodeURIComponent" -> #DESC:GLOBAL.decodeURIComponent
      "ArrayBuffer" -> #DESC:GLOBAL.ArrayBuffer
      "encodeURIComponent" -> #DESC:GLOBAL.encodeURIComponent
      "GetCapabilitiesExecutorFunctions" -> #DESC:GLOBAL.GetCapabilitiesExecutorFunctions
      "SharedArrayBuffer" -> #DESC:GLOBAL.SharedArrayBuffer
      "IfAbruptRejectPromise" -> #DESC:GLOBAL.IfAbruptRejectPromise
      "Math" -> #DESC:GLOBAL.Math
      "TypedArray" -> #DESC:GLOBAL.TypedArray
      "BigUint64Array" -> #DESC:GLOBAL.BigUint64Array
      "BigInt" -> #DESC:GLOBAL.BigInt
      "Uint8ClampedArray" -> #DESC:GLOBAL.Uint8ClampedArray
      "NaN" -> #DESC:GLOBAL.NaN
      "isNaN" -> #DESC:GLOBAL.isNaN
      "JSON" -> #DESC:GLOBAL.JSON
      "globalThis" -> #DESC:GLOBAL.globalThis
      "Infinity" -> #DESC:GLOBAL.Infinity
      "PromiseRejectFunctions" -> #DESC:GLOBAL.PromiseRejectFunctions
      "WeakMap" -> #DESC:GLOBAL.WeakMap
      "AggregateError" -> #DESC:GLOBAL.AggregateError
      "RangeError" -> #DESC:GLOBAL.RangeError
      "Int8Array" -> #DESC:GLOBAL.Int8Array
      "AsyncfromSyncIteratorValueUnwrapFunctions" -> #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions
      "Uint16Array" -> #DESC:GLOBAL.Uint16Array
      "decodeURI" -> #DESC:GLOBAL.decodeURI
      "DefaultConstructorFunctions" -> #DESC:GLOBAL.DefaultConstructorFunctions
      "AsyncGeneratorResumeNextReturnProcessorRejectedFunctions" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions
      "Reflect" -> #DESC:GLOBAL.Reflect
      "Number" -> #DESC:GLOBAL.Number
      "RegExp" -> #DESC:GLOBAL.RegExp
      "Symbol" -> #DESC:GLOBAL.Symbol
      "SyntaxError" -> #DESC:GLOBAL.SyntaxError
      "AsyncGeneratorFunction" -> #DESC:GLOBAL.AsyncGeneratorFunction
      "ProxyRevocationFunctions" -> #DESC:GLOBAL.ProxyRevocationFunctions
      "GeneratorFunction" -> #DESC:GLOBAL.GeneratorFunction
      "TypeError" -> #DESC:GLOBAL.TypeError
      "Proxy" -> #DESC:GLOBAL.Proxy
      "InternalizeJSONProperty" -> #DESC:GLOBAL.InternalizeJSONProperty
      "eval" -> #DESC:GLOBAL.eval
      "CatchFinallyFunctions" -> #DESC:GLOBAL.CatchFinallyFunctions
      "DataView" -> #DESC:GLOBAL.DataView
      "ThrowTypeError" -> #DESC:GLOBAL.ThrowTypeError
      "x" -> #39
      "parseFloat" -> #DESC:GLOBAL.parseFloat
      "Set" -> #DESC:GLOBAL.Set
      "Float32Array" -> #DESC:GLOBAL.Float32Array
      "ThenFinallyFunctions" -> #DESC:GLOBAL.ThenFinallyFunctions
      "AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions
      "Error" -> #DESC:GLOBAL.Error
      "WeakSet" -> #DESC:GLOBAL.WeakSet
      "EvalError" -> #DESC:GLOBAL.EvalError
      "AwaitRejectedFunctions" -> #DESC:GLOBAL.AwaitRejectedFunctions
      "Int32Array" -> #DESC:GLOBAL.Int32Array
      "URIError" -> #DESC:GLOBAL.URIError
      "String" -> #DESC:GLOBAL.String
      "Object" -> #DESC:GLOBAL.Object
      "Float64Array" -> #DESC:GLOBAL.Float64Array
      "Date" -> #DESC:GLOBAL.Date
      "Array" -> #DESC:GLOBAL.Array
      "Map" -> #DESC:GLOBAL.Map
      "Int16Array" -> #DESC:GLOBAL.Int16Array
      "__ABS__" -> #DESC:GLOBAL.__ABS__
      "HostPrint" -> #DESC:GLOBAL.HostPrint
      "ReferenceError" -> #DESC:GLOBAL.ReferenceError
      "CreateDataPropertyOnObjectFunctions" -> #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions
      "ArgSetter" -> #DESC:GLOBAL.ArgSetter
    }
    #GLOBAL.Object.freeze -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "freeze"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.freeze.SubMap
      "Code" -> λ(GLOBAL.Object.freeze)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.PromiseResolveFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.keys.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.keys.name
      "length" -> #DESC:GLOBAL.Array.prototype.keys.length
    }
    #GLOBAL.ArgSetter -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "ArgSetter"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.ArgSetter.SubMap
      "Code" -> λ(GLOBAL.ArgSetter)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.TypedArray.from.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "from"
      "Configurable" -> true
    }
    #GLOBAL.WeakSet -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "WeakSet"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakSet.SubMap
      "Code" -> λ(GLOBAL.WeakSet)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.AggregateError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AggregateError.prototype.name
      "constructor" -> #DESC:GLOBAL.AggregateError.prototype.constructor
      "message" -> #DESC:GLOBAL.AggregateError.prototype.message
    }
    #DESC:GLOBAL.Array.prototype.filter.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "filter"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.allSettled -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.allSettled
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.reduceRight.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "reduceRight"
      "Configurable" -> true
    }
    #GLOBAL.Object.getOwnPropertySymbols.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.getOwnPropertySymbols.name
      "length" -> #DESC:GLOBAL.Object.getOwnPropertySymbols.length
    }
    #GLOBAL.Array.prototype.lastIndexOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "lastIndexOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.lastIndexOf.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.lastIndexOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.values.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toFixed.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Boolean"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.apply.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.Object.isSealed.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.isSealed.name
      "length" -> #DESC:GLOBAL.Object.isSealed.length
    }
    #DESC:GLOBAL.Object.preventExtensions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakSet
      "Configurable" -> true
    }
    #GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions.SubMap
      "Code" -> λ(GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Number.isFinite.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.isFinite.name
      "length" -> #DESC:GLOBAL.Number.isFinite.length
    }
    #DESC:GLOBAL.Promise.race -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise.race
      "Configurable" -> true
    }
    #EXECUTION_STACK -> []
    #DESC:GLOBAL.Set.prototype.forEach -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Set.prototype.forEach
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.has.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.has.name
      "length" -> #DESC:GLOBAL.Set.prototype.has.length
    }
    #GLOBAL.Number.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.prototype.toString.name
      "length" -> #DESC:GLOBAL.Number.prototype.toString.length
    }
    #GLOBAL.Object.keys -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "keys"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.keys.SubMap
      "Code" -> λ(GLOBAL.Object.keys)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Generator.prototype.throw -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "throw"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Generator.prototype.throw.SubMap
      "Code" -> λ(GLOBAL.Generator.prototype.throw)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.HostPrint.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #28 -> ["x"]
    #GLOBAL.String -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "String"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.SubMap
      "Code" -> λ(GLOBAL.String)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.trim -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "trim"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.trim.SubMap
      "Code" -> λ(GLOBAL.String.prototype.trim)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Function.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Function.prototype.toString
      "Configurable" -> true
    }
    #GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AsyncfromSyncIteratorValueUnwrapFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions.SubMap
      "Code" -> λ(GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ReferenceError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.ReferenceError.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.AsyncFunction.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AsyncFunction.prototype
      "Configurable" -> false
    }
    #GLOBAL.WeakSet.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.WeakSet.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.AggregateError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AggregateError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AggregateError.SubMap
      "Code" -> λ(GLOBAL.AggregateError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Symbol"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.SubMap
      "Code" -> λ(GLOBAL.Symbol)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.TypedArray.of.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "of"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.sort -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.sort
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.parseFloat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.parseFloat
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.has.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "has"
      "Configurable" -> true
    }
    #DESC:GLOBAL.GetCapabilitiesExecutorFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "GetCapabilitiesExecutorFunctions"
      "Configurable" -> true
    }
    #GLOBAL.Object.assign -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "assign"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.assign.SubMap
      "Code" -> λ(GLOBAL.Object.assign)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Boolean -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Boolean
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getPrototypeOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.valueOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "valueOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.valueOf.SubMap
      "Code" -> λ(GLOBAL.String.prototype.valueOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map[SYMBOL_species] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get [Symbol.species]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map[SYMBOL_species].SubMap
      "Code" -> λ(GLOBAL.Map[SYMBOL_species])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.prototype.hasOwnProperty.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.prototype.hasOwnProperty.name
      "length" -> #DESC:GLOBAL.Object.prototype.hasOwnProperty.length
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_iterator] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.values
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.toPrecision.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Number.prototype.toPrecision.name
      "length" -> #DESC:GLOBAL.Number.prototype.toPrecision.length
    }
    #DESC:GLOBAL.Array.prototype.indexOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.DataView -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.DataView
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.localeCompare -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.localeCompare
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.entries -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.entries
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.any.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "any"
      "Configurable" -> true
    }
    #GLOBAL.CreateDataPropertyOnObjectFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "CreateDataPropertyOnObjectFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.CreateDataPropertyOnObjectFunctions.SubMap
      "Code" -> λ(GLOBAL.CreateDataPropertyOnObjectFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ReferenceError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ReferenceError
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.trim -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.trim
      "Configurable" -> true
    }
    #GLOBAL.Math -> (NotSupported "OrdinaryObject" "GLOBAL.Math")
    #GLOBAL.Number.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.Number.prototype
      "isFinite" -> #DESC:GLOBAL.Number.isFinite
      "MAX_VALUE" -> #DESC:GLOBAL.Number.MAX_VALUE
      "length" -> #DESC:GLOBAL.Number.length
      "MAX_SAFE_INTEGER" -> #DESC:GLOBAL.Number.MAX_SAFE_INTEGER
      "EPSILON" -> #DESC:GLOBAL.Number.EPSILON
      "parseFloat" -> #DESC:GLOBAL.Number.parseFloat
      "MIN_VALUE" -> #DESC:GLOBAL.Number.MIN_VALUE
      "name" -> #DESC:GLOBAL.Number.name
      "isSafeInteger" -> #DESC:GLOBAL.Number.isSafeInteger
      "POSITIVE_INFINITY" -> #DESC:GLOBAL.Number.POSITIVE_INFINITY
      "parseInt" -> #DESC:GLOBAL.Number.parseInt
      "NEGATIVE_INFINITY" -> #DESC:GLOBAL.Number.NEGATIVE_INFINITY
      "NaN" -> #DESC:GLOBAL.Number.NaN
      "isNaN" -> #DESC:GLOBAL.Number.isNaN
      "MIN_SAFE_INTEGER" -> #DESC:GLOBAL.Number.MIN_SAFE_INTEGER
      "isInteger" -> #DESC:GLOBAL.Number.isInteger
    }
    #GLOBAL.isNaN.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.isNaN.name
      "length" -> #DESC:GLOBAL.isNaN.length
    }
    #DESC:GLOBAL.String.prototype.includes -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.includes
      "Configurable" -> true
    }
    #47 -> (TYPE = ReferenceRecord) {
      "ThisValue" -> ~empty~
      "Base" -> N(#17)
      "Strict" -> true
      "ReferencedName" -> N("x")
    }
    #DESC:GLOBAL.Object.setPrototypeOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.entries -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.entries
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.apply -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Function.prototype.apply
      "Configurable" -> true
    }
    #GLOBAL.PromiseRejectFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.PromiseRejectFunctions.name
      "length" -> #DESC:GLOBAL.PromiseRejectFunctions.length
    }
    #GLOBAL.String.prototype.substring.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.substring.name
      "length" -> #DESC:GLOBAL.String.prototype.substring.length
    }
    #DESC:GLOBAL.parseInt -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.parseInt
      "Configurable" -> true
    }
    #GLOBAL.Array.of.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.of.name
      "length" -> #DESC:GLOBAL.Array.of.length
    }
    #DESC:GLOBAL.Number.MIN_SAFE_INTEGER -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> -9007199254740991i
      "Configurable" -> false
    }
    #DESC:GLOBAL.AwaitFulfilledFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AwaitFulfilledFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.lastIndexOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.lastIndexOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getOwnPropertyDescriptors.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "getOwnPropertyDescriptors"
      "Configurable" -> true
    }
    #GLOBAL.ForInIteratorPrototype.SubMap -> (TYPE = SubMap) {
      "next" -> #DESC:GLOBAL.ForInIteratorPrototype.next
    }
    #DESC:GLOBAL.Array.prototype.unshift.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.create -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "create"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.create.SubMap
      "Code" -> λ(GLOBAL.Object.create)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.MapIteratorPrototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Map Iterator"
      "Configurable" -> true
    }
    #GLOBAL.Object.create.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.create.name
      "length" -> #DESC:GLOBAL.Object.create.length
    }
    #DESC:GLOBAL.Promise[SYMBOL_species] -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Promise[SYMBOL_species]
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #GLOBAL.TypeError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.TypeError.prototype.name
      "constructor" -> #DESC:GLOBAL.TypeError.prototype.constructor
      "message" -> #DESC:GLOBAL.TypeError.prototype.message
    }
    #GLOBAL.Promise.prototype.finally -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "finally"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Promise.prototype.finally.SubMap
      "Code" -> λ(GLOBAL.Promise.prototype.finally)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.TypedArray.from.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.TypedArray.from.name
      "length" -> #DESC:GLOBAL.TypedArray.from.length
    }
    #62 -> []
    #DESC:GLOBAL.ThrowTypeError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "ThrowTypeError"
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.prototype.endsWith -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.endsWith
      "Configurable" -> true
    }
    #GLOBAL.HostPrint -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "HostPrint"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.HostPrint.SubMap
      "Code" -> λ(GLOBAL.HostPrint)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.CatchFinallyFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.CatchFinallyFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.get -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakMap.prototype.get
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].findIndex -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.SharedArrayBuffer -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.SharedArrayBuffer
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Boolean.prototype.toString
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.assign -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.assign
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.has -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakMap.prototype.has
      "Configurable" -> true
    }
    #34 -> ["x"]
    #GLOBAL.Object.setPrototypeOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "setPrototypeOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.setPrototypeOf.SubMap
      "Code" -> λ(GLOBAL.Object.setPrototypeOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.EvalError.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "EvalError"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.splice.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.splice.name
      "length" -> #DESC:GLOBAL.Array.prototype.splice.length
    }
    #DESC:GLOBAL.GetCapabilitiesExecutorFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.trimStart.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #PRIMITIVE -> (TYPE = PRIMITIVE) {
      "BigInt" -> #PRIMITIVE.BigInt
      "Number" -> #PRIMITIVE.Number
    }
    #DESC:GLOBAL.AsyncGeneratorFunction.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AsyncGeneratorFunction.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Map.prototype.size.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get size"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.set.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "set"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions.name
      "length" -> #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorRejectedFunctions.length
    }
    #GLOBAL.String.prototype.toLocaleLowerCase.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.toLocaleLowerCase.name
      "length" -> #DESC:GLOBAL.String.prototype.toLocaleLowerCase.length
    }
    #GLOBAL.AwaitFulfilledFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AwaitFulfilledFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AwaitFulfilledFunctions.SubMap
      "Code" -> λ(GLOBAL.AwaitFulfilledFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.endsWith.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.endsWith.name
      "length" -> #DESC:GLOBAL.String.prototype.endsWith.length
    }
    #DESC:GLOBAL.WeakSet.prototype.delete.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.charCodeAt.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.charCodeAt.name
      "length" -> #DESC:GLOBAL.String.prototype.charCodeAt.length
    }
    #DESC:GLOBAL.Function.prototype.arguments -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.ThrowTypeError
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> #GLOBAL.ThrowTypeError
    }
    #DESC:GLOBAL.Error.prototype.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> "Error"
      "Configurable" -> true
    }
    #GLOBAL.encodeURI.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.encodeURI.name
      "length" -> #DESC:GLOBAL.encodeURI.length
    }
    #DESC:GLOBAL.Map -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map
      "Configurable" -> true
    }
    #DESC:GLOBAL.Function.prototype.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.print.SubMap -> (TYPE = SubMap) {
      "length" -> #DESC:GLOBAL.print.length
    }
    #DESC:GLOBAL.Number.prototype.valueOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "valueOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.toLocaleLowerCase.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toLocaleLowerCase"
      "Configurable" -> true
    }
    #4 -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.ThrowTypeError
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> #GLOBAL.ThrowTypeError
    }
    #DESC:GLOBAL.Symbol.prototype.valueOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Symbol.prototype.valueOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Promise
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.fill.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "fill"
      "Configurable" -> true
    }
    #GLOBAL.Set.prototype.add.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.add.name
      "length" -> #DESC:GLOBAL.Set.prototype.add.length
    }
    #DESC:GLOBAL.BigInt.asUintN.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "asUintN"
      "Configurable" -> true
    }
    #GLOBAL.Object.fromEntries.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.fromEntries.name
      "length" -> #DESC:GLOBAL.Object.fromEntries.length
    }
    #GLOBAL.String.fromCharCode -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "fromCharCode"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.fromCharCode.SubMap
      "Code" -> λ(GLOBAL.String.fromCharCode)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.TypedArray[SYMBOL_species] -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "[Symbol.species]"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.TypedArray[SYMBOL_species].SubMap
      "Code" -> λ(GLOBAL.TypedArray[SYMBOL_species])
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.indexOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "indexOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.indexOf.SubMap
      "Code" -> λ(GLOBAL.String.prototype.indexOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.AsyncFunction.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.AsyncFunction.prototype
      "name" -> #DESC:GLOBAL.AsyncFunction.name
      "length" -> #DESC:GLOBAL.AsyncFunction.length
    }
    #GLOBAL.ReferenceError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.ReferenceError.prototype
      "name" -> #DESC:GLOBAL.ReferenceError.name
      "length" -> #DESC:GLOBAL.ReferenceError.length
    }
    #DESC:GLOBAL.Promise[SYMBOL_species].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.trimEnd.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.MapIteratorPrototype.next -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.MapIteratorPrototype.next
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.delete.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.ArrayIteratorPrototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.ArrayIteratorPrototype[SYMBOL_toStringTag]
      "next" -> #DESC:GLOBAL.ArrayIteratorPrototype.next
    }
    #6 -> ["Configurable", "Enumerable", "Get", "Set"]
    #DESC:GLOBAL.Number.prototype.toLocaleString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Array.of -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "of"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.of.SubMap
      "Code" -> λ(GLOBAL.Array.of)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.prototype.description -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "get description"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.prototype.description.SubMap
      "Code" -> λ(GLOBAL.Symbol.prototype.description)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.TypedArray.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Symbol.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Symbol.prototype.toString.name
      "length" -> #DESC:GLOBAL.Symbol.prototype.toString.length
    }
    #GLOBAL.ThrowTypeError.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ThrowTypeError.name
      "length" -> #DESC:GLOBAL.ThrowTypeError.length
    }
    #58 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> 3.0
      "Configurable" -> false
    }
    #GLOBAL.Function.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Function.prototype.toString.name
      "length" -> #DESC:GLOBAL.Function.prototype.toString.length
    }
    #DESC:GLOBAL.ThenFinallyFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "ThenFinallyFunctions"
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.get.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #ALGORITHM -> (TYPE = ALGORITHM) {}
    #DESC:GLOBAL.SyntaxError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.shift.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "shift"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map[SYMBOL_species] -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Map[SYMBOL_species]
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #DESC:GLOBAL.AsyncFunction.prototype[SYMBOL_toStringTag] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AsyncFunction"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.replaceAll -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.replaceAll
      "Configurable" -> true
    }
    #GLOBAL.Symbol.keyFor -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "keyFor"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Symbol.keyFor.SubMap
      "Code" -> λ(GLOBAL.Symbol.keyFor)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.findIndex.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #PRIMITIVE.BigInt -> (TYPE = Record) {
      "toString" -> λ(BigInt::toString)
      "leftShift" -> λ(BigInt::leftShift)
      "bitwiseXOR" -> λ(BigInt::bitwiseXOR)
      "exponentiate" -> λ(BigInt::exponentiate)
      "unsignedRightShift" -> λ(BigInt::unsignedRightShift)
      "bitwiseNOT" -> λ(BigInt::bitwiseNOT)
      "lessThan" -> λ(BigInt::lessThan)
      "remainder" -> λ(BigInt::remainder)
      "unit" -> 1n
      "bitwiseOR" -> λ(BigInt::bitwiseOR)
      "unaryMinus" -> λ(BigInt::unaryMinus)
      "divide" -> λ(BigInt::divide)
      "sameValueZero" -> λ(BigInt::sameValueZero)
      "equal" -> λ(BigInt::equal)
      "bitwiseAND" -> λ(BigInt::bitwiseAND)
      "multiply" -> λ(BigInt::multiply)
      "add" -> λ(BigInt::add)
      "signedRightShift" -> λ(BigInt::signedRightShift)
      "subtract" -> λ(BigInt::subtract)
      "sameValue" -> λ(BigInt::sameValue)
    }
    #DESC:GLOBAL.AsyncGeneratorFunction.prototype.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AsyncGenerator.prototype
      "Configurable" -> true
    }
    #DESC:GLOBAL.decodeURI.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "decodeURI"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array[SYMBOL_species].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype -> (TYPE = ArrayExoticObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.Array.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(ArrayExoticObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.String.prototype.padEnd -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.padEnd
      "Configurable" -> true
    }
    #GLOBAL.Map.prototype.clear -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "clear"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.clear.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.clear)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Generator.prototype.return -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "return"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Generator.prototype.return.SubMap
      "Code" -> λ(GLOBAL.Generator.prototype.return)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.join.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "join"
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "BigInt"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.pop -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "pop"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.pop.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.pop)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.fromEntries -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.fromEntries
      "Configurable" -> true
    }
    #DESC:GLOBAL.encodeURIComponent.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.RangeError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.RangeError.prototype
      "Configurable" -> false
    }
    #GLOBAL.String.prototype.localeCompare -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "localeCompare"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.localeCompare.SubMap
      "Code" -> λ(GLOBAL.String.prototype.localeCompare)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].flat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.prototype.valueOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.fromCodePoint.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "fromCodePoint"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set[SYMBOL_species].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get [Symbol.species]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.CatchFinallyFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.defineProperties.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.defineProperties.name
      "length" -> #DESC:GLOBAL.Object.defineProperties.length
    }
    #GLOBAL.Number.prototype.toFixed -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toFixed"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.prototype.toFixed.SubMap
      "Code" -> λ(GLOBAL.Number.prototype.toFixed)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.getOwnPropertyNames.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.defineProperties.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.Object.isFrozen.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.isFrozen.name
      "length" -> #DESC:GLOBAL.Object.isFrozen.length
    }
    #GLOBAL.Symbol.hasInstance -> (Symbol "Symbol.hasInstance")
    #DESC:GLOBAL.String.prototype.valueOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #INTRINSICS -> (TYPE = INTRINSICS) {}
    #DESC:GLOBAL.Number.prototype.toPrecision -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.prototype.toPrecision
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.charCodeAt.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.decodeURI -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "decodeURI"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.decodeURI.SubMap
      "Code" -> λ(GLOBAL.decodeURI)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.getPrototypeOf.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "getPrototypeOf"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.delete.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.throw.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Number.isFinite -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isFinite"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.isFinite.SubMap
      "Code" -> λ(GLOBAL.Number.isFinite)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.search -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "search"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.search.SubMap
      "Code" -> λ(GLOBAL.String.prototype.search)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #16 -> (TYPE = SubMap) {}
    #DESC:GLOBAL.Promise.prototype.then.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "then"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.prototype.then.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.repeat.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "repeat"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Int32Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Int32Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.hasOwnProperty.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "hasOwnProperty"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.isConcatSpreadable -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.isConcatSpreadable
      "Configurable" -> false
    }
    #GLOBAL.String.prototype.startsWith -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "startsWith"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.startsWith.SubMap
      "Code" -> λ(GLOBAL.String.prototype.startsWith)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.isFinite.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "isFinite"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Date -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Date
      "Configurable" -> true
    }
    #GLOBAL.GeneratorFunction.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.GeneratorFunction.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.reject.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "reject"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Boolean.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype.return -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "return"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AsyncGenerator.prototype.return.SubMap
      "Code" -> λ(GLOBAL.AsyncGenerator.prototype.return)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Set.prototype.clear.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Set.prototype.clear.name
      "length" -> #DESC:GLOBAL.Set.prototype.clear.length
    }
    #DESC:GLOBAL.Promise.prototype.catch.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "catch"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Uint8Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Uint8Array
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Array"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.iterator -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.iterator
      "Configurable" -> false
    }
    #DESC:GLOBAL.Object.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #18 -> ["x"]
    #DESC:GLOBAL.ArrayIteratorPrototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.valueOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.prototype.valueOf.name
      "length" -> #DESC:GLOBAL.Object.prototype.valueOf.length
    }
    #DESC:GLOBAL.AsyncGeneratorFunction -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncGeneratorFunction
      "Configurable" -> true
    }
    #GLOBAL.ReferenceError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.ReferenceError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.SyntaxError.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.SyntaxError.prototype
      "name" -> #DESC:GLOBAL.SyntaxError.name
      "length" -> #DESC:GLOBAL.SyntaxError.length
    }
    #DESC:GLOBAL.String.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].fill -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.keys.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #48 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #GLOBAL.WeakSet.prototype.delete -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "delete"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakSet.prototype.delete.SubMap
      "Code" -> λ(GLOBAL.WeakSet.prototype.delete)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.parseFloat.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "parseFloat"
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.map -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "map"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.map.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.map)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Map.prototype.get.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.prototype[SYMBOL_toPrimitive] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.prototype[SYMBOL_toPrimitive]
      "Configurable" -> true
    }
    #DESC:GLOBAL.GeneratorFunction.prototype.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Generator.prototype
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.every.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.some -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "some"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.some.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.some)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Symbol.matchAll -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Symbol.matchAll
      "Configurable" -> false
    }
    #DESC:GLOBAL.Promise.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Promise.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Boolean.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #63 -> (TYPE = ExecutionContext) {
      "Function" -> #GLOBAL.print
      "ScriptOrModule" -> null
      "Realm" -> absent
    }
    #DESC:GLOBAL.Atomics -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Atomics
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.copyWithin.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.copyWithin.name
      "length" -> #DESC:GLOBAL.Array.prototype.copyWithin.length
    }
    #GLOBAL.Map.prototype.values.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.values.name
      "length" -> #DESC:GLOBAL.Map.prototype.values.length
    }
    #DESC:GLOBAL.BigInt.asIntN.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.delete.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "delete"
      "Configurable" -> true
    }
    #GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions.name
      "length" -> #DESC:GLOBAL.AsyncfromSyncIteratorValueUnwrapFunctions.length
    }
    #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.isFinite -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isFinite"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.isFinite.SubMap
      "Code" -> λ(GLOBAL.isFinite)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Map.prototype.forEach.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Map.prototype.forEach.name
      "length" -> #DESC:GLOBAL.Map.prototype.forEach.length
    }
    #GLOBAL.Array.SubMap -> (TYPE = SubMap) {
      "prototype" -> #DESC:GLOBAL.Array.prototype
      "length" -> #DESC:GLOBAL.Array.length
      #GLOBAL.Symbol.species -> #DESC:GLOBAL.Array[SYMBOL_species]
      "name" -> #DESC:GLOBAL.Array.name
      "isArray" -> #DESC:GLOBAL.Array.isArray
      "of" -> #DESC:GLOBAL.Array.of
      "from" -> #DESC:GLOBAL.Array.from
    }
    #GLOBAL.Object.getOwnPropertyNames.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Object.getOwnPropertyNames.name
      "length" -> #DESC:GLOBAL.Object.getOwnPropertyNames.length
    }
    #DESC:GLOBAL.TypedArray.of -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.TypedArray.of
      "Configurable" -> true
    }
    #GLOBAL.BigInt.prototype.valueOf.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.BigInt.prototype.valueOf.name
      "length" -> #DESC:GLOBAL.BigInt.prototype.valueOf.length
    }
    #GLOBAL.Symbol.toPrimitive -> (Symbol "Symbol.toPrimitive")
    #DESC:GLOBAL.encodeURI.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "encodeURI"
      "Configurable" -> true
    }
    #DESC:GLOBAL.URIError.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.StringIteratorPrototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #DESC:GLOBAL.decodeURI -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.decodeURI
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.reject.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.map.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "map"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.keyFor.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "keyFor"
      "Configurable" -> true
    }
    #DESC:GLOBAL.undefined -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> undefined
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.prototype.replace.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "replace"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.allSettled.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.copyWithin -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "copyWithin"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.copyWithin.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.copyWithin)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Object.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Object.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.Array.prototype.concat.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "concat"
      "Configurable" -> true
    }
    #GLOBAL.encodeURIComponent.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.encodeURIComponent.name
      "length" -> #DESC:GLOBAL.encodeURIComponent.length
    }
    #DESC:GLOBAL.Number.prototype.toPrecision.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toPrecision"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.sort.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.ArgGetter.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.lastIndexOf.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Symbol.for.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Generator.prototype.throw.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.preventExtensions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "preventExtensions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.preventExtensions.SubMap
      "Code" -> λ(GLOBAL.Object.preventExtensions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #3 -> ["Configurable", "Enumerable", "Get", "Set"]
    #DESC:GLOBAL.String.prototype.toLocaleLowerCase.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toExponential -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.prototype.toExponential
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toExponential.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #46 -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> undefined
      "Configurable" -> false
    }
    #GLOBAL.BigInt.asUintN.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.BigInt.asUintN.name
      "length" -> #DESC:GLOBAL.BigInt.asUintN.length
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncGenerator.prototype.next.name
      "length" -> #DESC:GLOBAL.AsyncGenerator.prototype.next.length
    }
    #DESC:GLOBAL.Object.defineProperties.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "defineProperties"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Array.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.String.prototype.trimEnd -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.trimEnd
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.entries.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "entries"
      "Configurable" -> true
    }
    #GLOBAL.SyntaxError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.SyntaxError.prototype.name
      "constructor" -> #DESC:GLOBAL.SyntaxError.prototype.constructor
      "message" -> #DESC:GLOBAL.SyntaxError.prototype.message
    }
    #DESC:GLOBAL.Array.prototype.entries.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "entries"
      "Configurable" -> true
    }
    #GLOBAL.parseInt.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.parseInt.name
      "length" -> #DESC:GLOBAL.parseInt.length
    }
    #DESC:GLOBAL.Int8Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Int8Array
      "Configurable" -> true
    }
    #GLOBAL.Boolean.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Boolean.prototype.toString.name
      "length" -> #DESC:GLOBAL.Boolean.prototype.toString.length
    }
    #GLOBAL.AwaitFulfilledFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AwaitFulfilledFunctions.name
      "length" -> #DESC:GLOBAL.AwaitFulfilledFunctions.length
    }
    #DESC:GLOBAL.BigInt.prototype.valueOf -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt.prototype.valueOf
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.toLocaleLowerCase -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.toLocaleLowerCase
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.from -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.from
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.concat -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "concat"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.concat.SubMap
      "Code" -> λ(GLOBAL.String.prototype.concat)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Map.prototype.clear -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.clear
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.size -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Map.prototype.size
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #GLOBAL.ArrayBuffer -> (NotSupported "OrdinaryObject" "GLOBAL.ArrayBuffer")
    #GLOBAL.Generator.prototype.next -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "next"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Generator.prototype.next.SubMap
      "Code" -> λ(GLOBAL.Generator.prototype.next)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.String.prototype.slice -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "slice"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.slice.SubMap
      "Code" -> λ(GLOBAL.String.prototype.slice)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.reverse.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.reverse.name
      "length" -> #DESC:GLOBAL.Array.prototype.reverse.length
    }
    #DESC:GLOBAL.String.prototype.normalize.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.forEach.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.forEach.name
      "length" -> #DESC:GLOBAL.Array.prototype.forEach.length
    }
    #GLOBAL.WeakMap.prototype.has.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.WeakMap.prototype.has.name
      "length" -> #DESC:GLOBAL.WeakMap.prototype.has.length
    }
    #DESC:GLOBAL.Array.prototype.shift.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.trimEnd.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.trimEnd.name
      "length" -> #DESC:GLOBAL.String.prototype.trimEnd.length
    }
    #DESC:GLOBAL.GeneratorFunction.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.GeneratorFunction
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.throw.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "throw"
      "Configurable" -> true
    }
    #GLOBAL.AsyncGenerator.prototype.return.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncGenerator.prototype.return.name
      "length" -> #DESC:GLOBAL.AsyncGenerator.prototype.return.length
    }
    #DESC:GLOBAL.String.prototype.padStart.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "padStart"
      "Configurable" -> true
    }
    #DESC:GLOBAL.URIError.prototype -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.URIError.prototype
      "Configurable" -> false
    }
    #DESC:GLOBAL.print.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.SyntaxError -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "SyntaxError"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.SyntaxError.SubMap
      "Code" -> λ(GLOBAL.SyntaxError)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Error
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Symbol.search -> (Symbol "Symbol.search")
    #GLOBAL.AsyncFromSyncIteratorPrototype.return.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.return.name
      "length" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.return.length
    }
    #DESC:GLOBAL.SyntaxError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.SyntaxError
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.__ABS__.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Promise.allSettled.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.allSettled.name
      "length" -> #DESC:GLOBAL.Promise.allSettled.length
    }
    #DESC:GLOBAL.BigInt -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.BigInt
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.prototype.toString
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.seal -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Object.seal
      "Configurable" -> true
    }
    #GLOBAL.EvalError.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Error.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.EvalError.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.TypedArray.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "TypedArray"
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakSet.prototype.delete.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "delete"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Uint8ClampedArray -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Uint8ClampedArray
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype.toString.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toString"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Promise.prototype.finally.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "finally"
      "Configurable" -> true
    }
    #GLOBAL.ArrayIteratorPrototype.next.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.ArrayIteratorPrototype.next.name
      "length" -> #DESC:GLOBAL.ArrayIteratorPrototype.next.length
    }
    #GLOBAL.Promise.prototype.catch.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Promise.prototype.catch.name
      "length" -> #DESC:GLOBAL.Promise.prototype.catch.length
    }
    #DESC:GLOBAL.Promise[SYMBOL_species].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get [Symbol.species]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.TypedArray[SYMBOL_species].length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #GLOBAL.Array.prototype.toString.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.toString.name
      "length" -> #DESC:GLOBAL.Array.prototype.toString.length
    }
    #DESC:GLOBAL.Float32Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Float32Array
      "Configurable" -> true
    }
    #GLOBAL.WeakMap.prototype.set -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "set"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.WeakMap.prototype.set.SubMap
      "Code" -> λ(GLOBAL.WeakMap.prototype.set)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.AsyncFunction.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AsyncFunction
      "Configurable" -> true
    }
    #GLOBAL.EvalError.prototype.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.EvalError.prototype.name
      "constructor" -> #DESC:GLOBAL.EvalError.prototype.constructor
      "message" -> #DESC:GLOBAL.EvalError.prototype.message
    }
    #GLOBAL.String.prototype.padStart.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.padStart.name
      "length" -> #DESC:GLOBAL.String.prototype.padStart.length
    }
    #GLOBAL.Symbol.asyncIterator -> (Symbol "Symbol.asyncIterator")
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Array.prototype[SYMBOL_unscopables]
      "Configurable" -> true
    }
    #DESC:GLOBAL.ReferenceError.prototype.message -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> ""
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array[SYMBOL_species] -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.Array[SYMBOL_species]
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> undefined
    }
    #GLOBAL.Map.prototype.set -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "set"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Map.prototype.set.SubMap
      "Code" -> λ(GLOBAL.Map.prototype.set)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Promise.any.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.MapIteratorPrototype.next.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "next"
      "Configurable" -> true
    }
    #DESC:GLOBAL.ReferenceError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "ReferenceError"
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.return.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "return"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Proxy -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Proxy
      "Configurable" -> true
    }
    #35 -> ["x"]
    #DESC:GLOBAL.AsyncGenerator.prototype.throw -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.AsyncGenerator.prototype.throw
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.DefaultConstructorFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> false
    }
    #DESC:GLOBAL.Symbol.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Symbol
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.NaN -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> NaN
      "Configurable" -> false
    }
    #DESC:GLOBAL.Generator.prototype.throw.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "throw"
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.WeakMap
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].find -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.Generator.prototype.return -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Generator.prototype.return
      "Configurable" -> true
    }
    #DESC:GLOBAL.parseFloat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.parseFloat
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.charCodeAt.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "charCodeAt"
      "Configurable" -> true
    }
    #GLOBAL.AsyncFromSyncIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.AsyncIteratorPrototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.AsyncFromSyncIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.ProxyRevocationFunctions -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.ProxyRevocationFunctions
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.forEach -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Map.prototype.forEach
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.get.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "get"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.prototype.add.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "add"
      "Configurable" -> true
    }
    #DESC:GLOBAL.RangeError.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "RangeError"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.raw -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "raw"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.raw.SubMap
      "Code" -> λ(GLOBAL.String.raw)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #37 -> []
    #DESC:GLOBAL.Function.prototype[SYMBOL_hasInstance].name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "[Symbol.hasInstance]"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Map.prototype.set.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype -> (TYPE = StringExoticObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "StringData" -> ""
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(StringExoticObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(StringExoticObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.String.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(StringExoticObject.DefineOwnProperty)
    }
    #GLOBAL.CreateDataPropertyOnObjectFunctions.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions.name
      "length" -> #DESC:GLOBAL.CreateDataPropertyOnObjectFunctions.length
    }
    #DESC:GLOBAL.AwaitFulfilledFunctions.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "AwaitFulfilledFunctions"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Array.prototype[SYMBOL_unscopables].entries -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> true
      "Writable" -> true
      "Value" -> true
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.isInteger -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Number.isInteger
      "Configurable" -> true
    }
    #GLOBAL.Array -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Array"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.SubMap
      "Code" -> λ(GLOBAL.Array)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.unshift -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "unshift"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Array.prototype.unshift.SubMap
      "Code" -> λ(GLOBAL.Array.prototype.unshift)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.GeneratorFunction.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.next.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Set.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "Set"
      "Configurable" -> true
    }
    #GLOBAL.AwaitRejectedFunctions -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "AwaitRejectedFunctions"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.AwaitRejectedFunctions.SubMap
      "Code" -> λ(GLOBAL.AwaitRejectedFunctions)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.decodeURIComponent -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "decodeURIComponent"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.decodeURIComponent.SubMap
      "Code" -> λ(GLOBAL.decodeURIComponent)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Array.prototype.concat.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.concat.name
      "length" -> #DESC:GLOBAL.Array.prototype.concat.length
    }
    #DESC:GLOBAL.Promise.prototype.catch.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.BigInt.prototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.BigInt.prototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.WeakSet.prototype.has.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "has"
      "Configurable" -> true
    }
    #DESC:GLOBAL.IfAbruptRejectPromise.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 2.0
      "Configurable" -> true
    }
    #GLOBAL.AsyncFunction.prototype.SubMap -> (TYPE = SubMap) {
      #GLOBAL.Symbol.toStringTag -> #DESC:GLOBAL.AsyncFunction.prototype[SYMBOL_toStringTag]
      "constructor" -> #DESC:GLOBAL.AsyncFunction.prototype.constructor
    }
    #DESC:GLOBAL.JSON -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.JSON
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.codePointAt -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.codePointAt
      "Configurable" -> true
    }
    #GLOBAL.Function.prototype[SYMBOL_hasInstance].SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Function.prototype[SYMBOL_hasInstance].name
      "length" -> #DESC:GLOBAL.Function.prototype[SYMBOL_hasInstance].length
    }
    #GLOBAL.String.prototype.codePointAt -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "codePointAt"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.String.prototype.codePointAt.SubMap
      "Code" -> λ(GLOBAL.String.prototype.codePointAt)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Array.prototype.toString -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Array.prototype.toString
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.normalize.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "normalize"
      "Configurable" -> true
    }
    #GLOBAL.AsyncFromSyncIteratorPrototype.throw.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.throw.name
      "length" -> #DESC:GLOBAL.AsyncFromSyncIteratorPrototype.throw.length
    }
    #GLOBAL.String.prototype.trimStart.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.trimStart.name
      "length" -> #DESC:GLOBAL.String.prototype.trimStart.length
    }
    #GLOBAL.Symbol.SubMap -> (TYPE = SubMap) {
      "keyFor" -> #DESC:GLOBAL.Symbol.keyFor
      "asyncIterator" -> #DESC:GLOBAL.Symbol.asyncIterator
      "unscopables" -> #DESC:GLOBAL.Symbol.unscopables
      "length" -> #DESC:GLOBAL.Symbol.length
      "hasInstance" -> #DESC:GLOBAL.Symbol.hasInstance
      "toPrimitive" -> #DESC:GLOBAL.Symbol.toPrimitive
      "split" -> #DESC:GLOBAL.Symbol.split
      "replace" -> #DESC:GLOBAL.Symbol.replace
      "search" -> #DESC:GLOBAL.Symbol.search
      "isConcatSpreadable" -> #DESC:GLOBAL.Symbol.isConcatSpreadable
      "toStringTag" -> #DESC:GLOBAL.Symbol.toStringTag
      "prototype" -> #DESC:GLOBAL.Symbol.prototype
      "match" -> #DESC:GLOBAL.Symbol.match
      "iterator" -> #DESC:GLOBAL.Symbol.iterator
      "name" -> #DESC:GLOBAL.Symbol.name
      "for" -> #DESC:GLOBAL.Symbol.for
      "species" -> #DESC:GLOBAL.Symbol.species
      "matchAll" -> #DESC:GLOBAL.Symbol.matchAll
    }
    #GLOBAL.Array.prototype.sort.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.sort.name
      "length" -> #DESC:GLOBAL.Array.prototype.sort.length
    }
    #GLOBAL.String.prototype.concat.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.concat.name
      "length" -> #DESC:GLOBAL.String.prototype.concat.length
    }
    #GLOBAL.Array.prototype.fill.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.Array.prototype.fill.name
      "length" -> #DESC:GLOBAL.Array.prototype.fill.length
    }
    #GLOBAL.Object -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "Object"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.SubMap
      "Code" -> λ(GLOBAL.Object)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Prototype" -> #GLOBAL.Function.prototype
      "Construct" -> λ(BuiltinFunctionObject.Construct)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.Object.getOwnPropertyNames -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "getOwnPropertyNames"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.getOwnPropertyNames.SubMap
      "Code" -> λ(GLOBAL.Object.getOwnPropertyNames)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #GLOBAL.eval.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.eval.name
      "length" -> #DESC:GLOBAL.eval.length
    }
    #DESC:GLOBAL.Object.prototype.hasOwnProperty.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.prototype.toExponential.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "toExponential"
      "Configurable" -> true
    }
    #DESC:GLOBAL.WeakMap.prototype.has.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.String.prototype.search.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.prototype.search.name
      "length" -> #DESC:GLOBAL.String.prototype.search.length
    }
    #GLOBAL.decodeURIComponent.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.decodeURIComponent.name
      "length" -> #DESC:GLOBAL.decodeURIComponent.length
    }
    #GLOBAL.Proxy -> (NotSupported "OrdinaryObject" "GLOBAL.Proxy")
    #DESC:GLOBAL.Array.prototype.findIndex.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "findIndex"
      "Configurable" -> true
    }
    #DESC:GLOBAL.String.prototype.repeat -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.String.prototype.repeat
      "Configurable" -> true
    }
    #GLOBAL.Number.prototype.toPrecision -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "toPrecision"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.prototype.toPrecision.SubMap
      "Code" -> λ(GLOBAL.Number.prototype.toPrecision)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Map.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.EvalError -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.EvalError
      "Configurable" -> true
    }
    #DESC:GLOBAL.isFinite -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.isFinite
      "Configurable" -> true
    }
    #GLOBAL.Int16Array -> (NotSupported "OrdinaryObject" "GLOBAL.Int16Array")
    #DESC:GLOBAL.SyntaxError.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.SyntaxError
      "Configurable" -> true
    }
    #DESC:GLOBAL.Object.getOwnPropertyNames.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "getOwnPropertyNames"
      "Configurable" -> true
    }
    #2 -> (TYPE = PropertyDescriptor) {
      "Get" -> #GLOBAL.ThrowTypeError
      "Enumerable" -> false
      "Configurable" -> true
      "Set" -> #GLOBAL.ThrowTypeError
    }
    #GLOBAL.Object.isExtensible -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isExtensible"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.isExtensible.SubMap
      "Code" -> λ(GLOBAL.Object.isExtensible)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Function.prototype[SYMBOL_hasInstance] -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.Function.prototype[SYMBOL_hasInstance]
      "Configurable" -> false
    }
    #DESC:GLOBAL.AsyncGenerator.prototype.constructor -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> #GLOBAL.AsyncGeneratorFunction.prototype
      "Configurable" -> true
    }
    #DESC:GLOBAL.AsyncGeneratorResumeNextReturnProcessorFulfilledFunctions.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.AsyncIteratorPrototype -> (TYPE = OrdinaryObject) {
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Object.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "SubMap" -> #GLOBAL.AsyncIteratorPrototype.SubMap
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Int16Array -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> true
      "Value" -> #GLOBAL.Int16Array
      "Configurable" -> true
    }
    #GLOBAL.Number.isSafeInteger -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isSafeInteger"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Number.isSafeInteger.SubMap
      "Code" -> λ(GLOBAL.Number.isSafeInteger)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
    #DESC:GLOBAL.Symbol.prototype.toString.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 0.0
      "Configurable" -> true
    }
    #DESC:GLOBAL.BigInt.asIntN.name -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> "asIntN"
      "Configurable" -> true
    }
    #DESC:GLOBAL.Number.MAX_SAFE_INTEGER -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 9007199254740991i
      "Configurable" -> false
    }
    #GLOBAL.String.fromCodePoint.SubMap -> (TYPE = SubMap) {
      "name" -> #DESC:GLOBAL.String.fromCodePoint.name
      "length" -> #DESC:GLOBAL.String.fromCodePoint.length
    }
    #DESC:GLOBAL.Array.length -> (TYPE = PropertyDescriptor) {
      "Enumerable" -> false
      "Writable" -> false
      "Value" -> 1.0
      "Configurable" -> true
    }
    #GLOBAL.Object.prototype.isPrototypeOf -> (TYPE = BuiltinFunctionObject) {
      "SetPrototypeOf" -> λ(OrdinaryObject.SetPrototypeOf)
      "Delete" -> λ(OrdinaryObject.Delete)
      "Prototype" -> #GLOBAL.Function.prototype
      "IsExtensible" -> λ(OrdinaryObject.IsExtensible)
      "InitialName" -> "isPrototypeOf"
      "OwnPropertyKeys" -> λ(OrdinaryObject.OwnPropertyKeys)
      "Call" -> λ(BuiltinFunctionObject.Call)
      "SubMap" -> #GLOBAL.Object.prototype.isPrototypeOf.SubMap
      "Code" -> λ(GLOBAL.Object.prototype.isPrototypeOf)
      "ScriptOrModule" -> null
      "HasProperty" -> λ(OrdinaryObject.HasProperty)
      "Get" -> λ(OrdinaryObject.Get)
      "PreventExtensions" -> λ(OrdinaryObject.PreventExtensions)
      "GetOwnProperty" -> λ(OrdinaryObject.GetOwnProperty)
      "Realm" -> #REALM
      "Extensible" -> true
      "Set" -> λ(OrdinaryObject.Set)
      "GetPrototypeOf" -> λ(OrdinaryObject.GetPrototypeOf)
      "DefineOwnProperty" -> λ(OrdinaryObject.DefineOwnProperty)
    }
  }
  filename: sample.js
}
```