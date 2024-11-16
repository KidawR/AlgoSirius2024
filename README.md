1.(Seminar1)

    def reverse(self):
        prev = None
        current = self.head
        while current is not None:
            next_node = current.next
            current.next = prev
            prev = current
            current = next_node
        self.head = prev

Алгоритмичная сложность O(N)-алгоритм проходит по списку один раз направление его указателей

Затраты по памяти O(1) - используется переменная для того чтобы хранить указатель на предидущий эллемент


3.(Seminar4)

    def invert_tree(self):
        self.root = self.__invert_tree(self.root)
    
    def __invert_tree(self, node):
        if node is None:
            return None
        # Меняем местами левого и правого потомков
        node.left, node.right = node.right, node.left
        # Рекурсивно инвертируем левого и правого потомков
        self.__invert_tree(node.left)
        self.__invert_tree(node.right)
        return node

Алгоритмическая сложность O(N)-алгоритм проходит по каждому узлу дерева один раз

Затраты по памяти O(N)-используется N уровней дерева для рекурсии

7.(Lab7)

Алгоритмическая сложность O(N^2)-алгоритм проходит по всем ребрам(E) графа для каждой вершины(V)

Затраты по памяти O(2N)-хранится массив расстояний(для каждой вершины O(v) памяти) и список ребер O(E)