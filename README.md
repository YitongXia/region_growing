# region growing

## This repository is used on the .off file where the surfaces are quite split, which mainly utilizes CGAL 5.5.2's Shape Detection.


Edge-adjacent faces are found using the internal face graph connectivity, while the RegionType related class depends on three parameters:

- distance_threshold - the maximum distance from the furthest face vertex to a plane;

- angle_threshold - the maximum accepted angle between the face normal and the normal of a plane;

- min_region_size - the minimum number of mesh faces a region must have.

The first two parameters are used by the functions RegionType::is_part_of_region() and RegionType::update(), while the third parameter is used by the function RegionType::is_valid_region() explained in Section Framework Regions. The right choice of these parameters is as important as the one explained in Section Parameters For Region Growing On Point Set.
