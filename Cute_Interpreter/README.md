# Cute_Interpreter
프로그래밍 언어개론 텀 프로젝트 - Item1, Item2, Item3

팀명 : 쫄리면 당신이 하시는게 어때요?
팀원 : 김수진, 김혁진


Item1 이후 구현 설명 :

class KeywordTable(object):
table = {}
	define한 값의 key와 value를 저장해두어 나중에 꺼내서 값을 얻을수 있게함.
lambdatalbe = {}
	lambda의 함수를 저장해서 나중에 계산 할 수 있게 할 생각
temptable = {}
	lambda에서 함수에 값을 넣으려면 x같은 미지수에 상수를 넣어야하는데
	이 때에 define이라 겹치면 안되니까 temptable을 만들어 미지수 값을
	저장하고 define처럼 쓰지만 define과 겹치지 않게 할 생각.
lamdakey = 0
	0에서 점점 ++ 시키면서 lamdakey를 각각 주어 lamda를 정의할 때의 
	서로 구분을 맡을 예정
	이 값은 lamdatable의 key에 넣을 생각임.


class Node(object): 내부

lookupTable(self):
	Node class 내에서 이 노드가 define되있는 노드인지 확인
	table의 key에 들어있는 value인지 확인함.

lookupLambda(self):
	lambda도 define처럼 lookuptable을 하는것처럼 사용할수 있지 않을까해서
	만듦.


def run_func(op_code_node):

l_node는 keyword 바로 앞에 오는 노드,
r_node는 l_node의 뒤에 오는 노드로 사용.

def define(node):
	l_node와 r_node를 정의한 후 r_node를 run_expr을 돌린 값을 넣어줌.

	**** l_node도 run_expr해야될 것같음. 
	car, cdr등의 값이 나올 경우도 있음!!!!!!

def lamda(node):
	lambda라는 이름이 기존의 함수가 있는듯.. 겹쳐서 lamda로 씀;;
	아직 미구현, print는 debug용으로 썼음..

def insert_lamdatable(id, value):
	define처럼 사용하기 위함.
	아직 미구현.

def insert_table(id, value):
	Keyword의 table에 l_node의 value를 key로 쓰고 r_node의 값을 저장해둠.
	후에 define된 값이 key로 사용되므로 key를 통해 값을 찾을 수 있음.


table['define'] = define
table['lambda'] = lamda
	여기서 사람이 써주는 값은 lambda이지만 함수이름은 lamda가 되도 되게만듦


run_expr(root_node):
	
root_node.lookupTable()
	여기서 이 노드가 define된 값인지 확인한다.

뒤에 있는 KeywordTable.table.keys()이 부분은 지워도 될것임.


def print_node(node):

if node.type is TokenType.DEFINE:
	return 'define'

	이 후 LAMBDA도 return 'lambda' 하게 만들어야할 것





