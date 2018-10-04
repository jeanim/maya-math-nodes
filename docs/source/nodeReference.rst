.. _nodeReference:

Node Reference
==============

Overview
********

The nodes are designed with the following principles in mind:

- nodes perform a single operation
- nodes have a single output attribute
- nodes are strongly typed

.. note::
   In order to achieve consistency and streamlined workflow, there are a few nodes that duplicate existing Maya functionality.

The node library tries to adhere to the following set of rules when it comes to choosing the node and attribute names:

- node names are prefixed with :code:`math_`
- nodes are named with affirmative action verbs, ex: :code:`Add`, :code:`Multiply`
- the `get` action verb is implied, ex: :code:`GetDotProduct` is :code:`DotProduct`
- nodes are assumed to operate on doubles by default, ex: :code:`Add`, :code:`Multiply`
- mixed type operations are reflected in the name, ex: :code:`AddVector`, :code:`MultiplyVectorByMatrix`
- conversion nodes have following format `OutputFromSource`, ex: :code:`RotationFromMatrix`
- attributes are generally named :code:`input` and :code:`output`
- if multiple inputs are required they are enumerated, ex: :code:`input1`, :code:`input2`
- for clarity other attribute names are allowed, ex: :code:`translation`, :code:`alpha`, :code:`axis`, :code:`min`


Node List
*********

Absolute
--------
:description: Computes absolute value
:type variants: AbsoluteAngle, AbsoluteInt
:expression: abs(x)

Acos
----
:description: Computes arccosine
:expression: acos(x)

Add
---
:description: Computes sum of two values
:type variants: AddAngle, AddInt, AddVector
:expression: x + y

AndBool
-------
:description: Gets logical *and* of two values
:type variants: AndInt

AngleBetweenVectors
-------------------
:description: Computes angle between two vectors
:expression: anglebetween(x, y)

Asin
----
:description: Computes arcsine
:expression: asin(x)

Atan
----
:description: Computes arctangent
:expression: atan(x)

Atan2
-----
:description: Computes arctangent of `x / y`
:expression: atan(x, y)

Average
-------
:description: Computes average value
:type variants: AverageAngle, AverageInt, AverageMatrix, AverageQuaternion, AverageRotation, AverageVector

AxisFromMatrix
--------------
:description: Gets basis vector from matrix for a given axis
:expression: axis(x, axis)

Ceil
----
:description: Computes the smallest integer value greater than or equal to input
:type variants: CeilAngle
:expression: ceil(x)

Clamp
-----
:description: Computes the value within the given min and max range
:type variants: ClampAngle, ClampInt
:expression: clamp(x, min, max)

Compare
-------
:description: Compute how the two values compare to each other
:type variants: CompareAngle
:expression: compare(x, y)

CosAngle
--------
:description: Computes the cosine of angle
:expression: cos(x)

CrossProduct
------------
:description: Computes the cross product of two vectors
:expression: cross(x, y)

Divide
------
:description: Computes the quotient of two values
:type variants: DivideAngle, DivideAngleByInt, DivideByInt
:expression: x / y

DotProduct
----------
:description: Computes the dot product of two vectors
:expression: dot(x, y)

DistancePoints
--------------
:description: Computes the distance between two points or matrices
:type variants: DistanceTransforms
:expression: distance(x, y)

Floor
-----
:description: Computes the largest integer value less than or equal to input
:expression: floor(x)

InverseMatrix
-------------
:description: Computes the inverse of value
:type variants: InverseQuaternion, InverseRotation
:expression: inverse(x)

Lerp
----
:description: Computes linear interpolation between two values
:type variants: LerpAngle, LerpMatrix, LerpVector
:expression: lerp(x, y, alpha)

MatrixFromTRS
-------------
:description: Computes a matrix from translation, rotation and scale

Max
---
:description: Gets the largest of the two values
:type variants: MaxAngle, MaxInt
:expression: max(x, y)

MaxElement
----------
:description: Gets the largest value in array
:type variants: MaxAngleElement, MaxIntElement
:expression: maxelement(x, y)

Min
---
:description: Gets the smallest of the two values
:type variants: MaxAngle, MaxInt
:expression: min(x, y)

MinElement
----------
:description: Gets the smallest value in array
:type variants: MinAngleElement, MinIntElement
:expression: minelement(x, y)

ModulusInt
----------
:description: Computes the remainder of the two values
:expression: x % y

Multiply
--------
:description: Computes the product of two values
:type variants: MultiplyAngle, MultiplyAngleByInt, MultiplyByInt, MultiplyInt, MultiplyMatrix,
   MultiplyQuaternion, MultiplyRotation, MultiplyVector, MultiplyVectorByMatrix
:expression: x * y

Negate
------
:description: Computes the negation of value
:type variants: NegateAngle, NegateInt, NegateVector
:expression: negate(x)

NormalizeVector
---------------
:description: Computes normalized vector
:expression: normalize(x)

NormalizeArray
---------------
:description: Normalize array of values
:expression: normalizearray(x)

NormalizeWeightsArray
---------------------
:description: Normalize array of weight values

OrBool
-------
:description: Gets logical *or* of two values
:type variants: OrInt

Power
-----
:description: Computes the value raised to power of the exponent
:expression: power(x, exp)

QuaternionFromMatrix
--------------------
:description: Gets quaternion from matrix or rotation
:type variants: QuaternionFromRotation
:expression: quat(x, rot_order)

Round
-----
:description: Computes rounded value
:type variants: RoundAngle
:expression: round(x)

RotationFromMatrix
------------------
:description: Gets rotation from matrix or quaternion
:type variants: RotationFromQuaternion
:expression: rot(x, rot_order)

ScaleFromMatrix
---------------
:description: Gets scale from matrix

Select
------
:description: Toggles output
:type variants: SelectAngle, SelectInt, SelectMatrix, SelectQuaternion, SelectRotation,
   SelectVector
:expression: select(x, y, state)

SelectArray
-----------
:description: Toggles array output
:type variants: SelectAngleArray, SelectIntArray, SelectMatrixArray, SelectVectorArray

SinAngle
--------
:description: Computes sin of angle
:expression: sin(x)

SlerpQuaternion
---------------
:description: Comptues slerp interpolation between two quaternions
:expression: slerp(x, y)

Subtract
--------
:description: Computes the difference between two values
:type variants: SubtractAngle, SubtractInt, SubtractVector
:expression: x - y

Sum
---
:description: Computes the the sum of values
:type variants: SumAngle, SumInt, SumVector

TanAngle
--------
:description: Computes tangent of angle
:expression: tan(x)

TranslationFromMatrix
---------------------
:description: Get translation from matrix

TwistFromMatrix
---------------
:description: Computes twist around axis from matrix or rotation
:type variants: TwistFromRotaiton
:expression: twist(x, axis, rot_order)

VectorLength
------------
:description: Computes length of vector
:expression: length(x)

VectorLengthSquared
-------------------
:description: Computes squared length of vector
:expression: lengthsquared(x)

WeightedAverage
---------------
:description: Computes the weighted average value
:type variants: WeightedAverageAngle, WeightedAverageInt, WeightedAverageMatrix, WeightedAverageQuaternion,
   WeightedAverageRotation, WeightedAverageVector

XorBool
-------
:description: Gets logical *xor* of two values
:type variants: XorInt
