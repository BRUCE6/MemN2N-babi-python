## python -m demo.qa
parser.add_argument("-d", "--data-dir", default="data/tasks_1-20_v1-2/en",
                        help="path to dataset directory (default: %(default)s)")
parser.add_argument("-m", "--model-file", default="trained_model/memn2n_model.pklz",
                    help="model file (default: %(default)s)")
group = parser.add_mutually_exclusive_group()
group.add_argument("-train", "--train", action="store_true",
                   help="train model (default: %(default)s)")
group.add_argument("-console", "--console-demo", action="store_true",
                   help="run console-based demo (default: %(default)s)")
group.add_argument("-web", "--web-demo", action="store_true", default=True,
                   help="run web-based demo (default: %(default)s)")
