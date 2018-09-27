# cmms
CEDA Manual Metadata Store (CMMS) holds YAML files for CEDA data catalogue records (matched by the file name and record uuid being the same) containing metadata information to be harvested along side content from other pollable metadata stores.


# example CMMS YAML
# contains all fields that can be used as
# a template, though not all are required.

# default rule is that the content are
# 'default' option selected if nothing comes back
# from the equivalent pollable metadata service (e.g. fbi, securityDB)

splice rules:
  phenomena: cmms_only

# a list of items, one per phenomena
# each element can be just 
# a name or could be a dictionary where
# more information can be given as a group
# in the example below 'Air Temperature' will be the display name 
# with associated entries being items from a vocab
# 'names' is used where there are a list of names to consider
#

phenomena:
- Air Temperature:
    gcmd_name: Air Temperature
    gcmd_url: http://vocab.ndg.nerc.ac.uk/term/P141/4/GVAR0027
    names:
    - Air Temperature
- Vertical Profile Of Air Temperature

# dates are in yyyy-mm-dd hh:mm:ss format
# if only start is given then it's an ongoing dataset
time_range:
    start: 
    end: 

# w-e is within -180 to 180 degrees lon
bbox:
    north: 
    east: 
    west: 
    south:

# float <units from b|kb|mb|gb|tb>, e.g. 4.392 gb
size: 

# int num of files
n_files: 

# one of: public|registered|restricted
accessType: 

# if accessType is 'restricted' then the access roles need to be
# defined in a list
accessRoles:
    - <1st group>
    - <2nd group>

# url to licence  
licenceUrl: 
